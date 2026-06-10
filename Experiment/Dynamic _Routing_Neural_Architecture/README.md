# Dynamic Routing Neural Architecture

A  neural architecture where computation depth and path are emergent rather than fixed. A small pool of shared functional units cooperate through attention-based autoregressive routing to solve tasks — no path supervision required.

---

## Core Idea

Most neural architectures fix structure and learn weights. This one learns both — the weights inside units and the computational graph itself.

A set of small functional units process input sequentially. After each unit, an attention mechanism decides which unit to visit next — the same way a transformer predicts the next token. Computation terminates when an output unit wins the attention. Depth and path are fully emergent.

---

## Architecture

Every functional unit has three parts:

- **Head** — generates a Key representing what this unit offers. Derived from the unit's own weights — so the key reflects actual capability, not an arbitrary embedding
- **Body** — MLP transformation. Receives `concat(prev_output, original_input)` — the original input is re-injected at every unit so no unit loses sight of the problem
- **Tail** — generates a Query from `concat(body_out, original_input)`. Attends over all unit Heads to select the next unit

**Input unit** — Body + Tail only. No Head — it is always first. Generates the first Query to kick off routing.

**Output unit** — Head + Body only. No Tail — terminal sink. Competes in every routing step. When it wins, computation terminates.

**Key property:** The same unit visited twice produces different computation because the Query changes each step. So AB ≠ BA — path order carries meaning. Paths like A → B → A → C are valid and meaningful.

---

## Routing Mechanism

```
# At each step:
Q = Tail(concat(body_out, original_input))   # what I did + where we started
K = Head(unit_weights)                        # what each unit offers

scores     = Q @ K.T / temperature            # attend over all units
selected   = Gumbel-Softmax(scores, hard=True) # discrete but differentiable

# Run all units in parallel, select winner via weights
# Accumulate output when output unit wins
# Repeat until output unit fires
```

Gumbel-Softmax with `hard=True` gives discrete routing decisions during the forward pass while keeping gradients flowing during training — no straight-through estimator needed separately.

---

## Key Findings

### Finding 1 — Capacity constraint is the primary inductive bias for routing

Reducing hidden dimension from 6 to 4 (2x input dimension) was the single most impactful change. With dim=6, one unit dominates and approximates all transformations alone. With dim=4, no unit can solve tasks independently — cooperation emerges naturally.

> Units specialize not because we forced them to, but because they have no other choice.

### Finding 2 — Entropy bonus provides meaningful secondary benefit

Without entropy regularization, routing is less consistent and occasional catastrophic failures appear (MSE > 2.0 on individual samples). With it, routing stabilizes and loss reaches 0.08 consistently.

### Finding 3 — Step penalty is unnecessary

An explicit penalty for early termination adds no benefit when capacity constraint is active. The architecture naturally maintains appropriate path depth without it.

---

## Ablation Results

All runs: 500 epochs, 3 functional units, 2D geometric input, synthetic 3-task dataset.

| Run | hidden_dim | entropy_w | step_penalty_w | Final Loss | Avg Steps | Notes                   |
|-----|------------|-----------|----------------|------------|-----------|-------------------------|
| 1   | 6          | 0.01      | 0.10           | 0.22       | 2.70      | one unit dominates      |
| 2   | 4          | 0.01      | 0.10           | 0.09       | 2.00      | cooperation emerges     |
| 3   | 4          | 0.01      | 0.00           | 0.08       | 2.00      | step penalty redundant  |
| 4   | 4          | 0.00      | 0.00           | 0.22       | 2.20      | entropy matters         |
| **5 (final)** | **4** | **0.01** | **0.00** | **0.08** | **2.00** | **final config** |

---

## Toy Task

Synthetic dataset of 2D geometric points. Task is determined by the angle of the input point — geometry alone determines the required transformation, no task label given to the network.

```
angle < 120°:  y = scale(rotate(x))           # requires 2 hops
angle < 240°:  y = reflect(scale(x))          # requires 2 hops
angle ≥ 240°:  y = scale(reflect(rotate(x))) # requires 3 hops
```

Three structurally different tasks, same input space. No one-hot task indicator — the network must route purely from geometry.

**Why this is a valid test:** A single capacity-constrained unit cannot approximate all three transformations. Routing must emerge for the network to solve the task.

---

## Sample Routing Inspection (final config, 500 epochs)

```
Task 0 (rotate→scale):     always routes [3, 0]      MSE ~0.003
Task 1 (scale→reflect):    routes [3, 2, 0] or [0]   MSE ~0.005
Task 2 (rotate→reflect→scale): always routes [1, 0]  MSE ~0.001
```

Routing is consistent per task — same input region always takes the same path. Different tasks take different paths. The output unit learned to solve some inputs directly with zero functional units — adaptive computation depth working as intended.

---

## How to Run

```bash
pip install torch numpy matplotlib

python dynamic_routing.py
```

Output: training loss/entropy table, routing inspection per task, saved plot of loss curves and path length visualization.

To reproduce any ablation run, change the config block at the top of the file:

```python
CONFIG = {
    "hidden_dim"      : 4,
    "entropy_w"       : 0.01,
    "step_penalty_w"  : 0.0,
    "epochs"          : 500,
    "lr"              : 1e-3,
}
```

---

## Limitations and Open Questions

- Validated on synthetic data only — generalization to real tasks unknown
- 3 functional units — scaling behavior unstudied
- Routing paths don't match ground truth exactly — network finds valid alternative solutions, not necessarily the designed ones
- Task 1 (reflect→scale) shows occasional routing inconsistency — the hardest task for this configuration

---

## Next Experiments

- Scale unit pool to 6-8 units — does specialization still emerge?
- Harder tasks requiring 4+ hops — does emergent depth scale?
- Visualize routing by input region — do routing boundaries align with task boundaries?
- Unit specialization analysis — do units develop interpretable roles?
- KL-based incremental change penalty — constrain how much any single unit can transform the representation

---

## What This Is Not

This is  not a production system. The claim is narrow and honest: a small pool of capacity-constrained shared units with attention-based autoregressive routing learns to cooperate and specialize without path supervision, proved on a synthetic 3-task geometric dataset.

---

*code can be ugly. hop you dont mind. Every design decision made from first principles.*
