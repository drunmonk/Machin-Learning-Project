# Makemore Part 4: Becoming a Backprop Ninja

> Part of Andrej Karpathy's [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) series.

## 📺 Overview

This notebook follows [**Building makemore Part 4: Becoming a Backprop Ninja**](https://www.youtube.com/watch?v=q8SA3rM6ckI) by Andrej Karpathy.

We take the 2-layer MLP with BatchNorm from Part 3 and **manually backpropagate** through the entire network — without using PyTorch's `loss.backward()`. The goal is to build deep intuition about how gradients flow through a compute graph at the level of efficient Tensors (not just individual scalars like in micrograd).

---

## 🧠 What's Covered

Manual backward pass through each component of the network, in order:

1. **Cross Entropy Loss** — backward through the fused softmax + NLL loss
2. **2nd Linear Layer** — `dL/dW`, `dL/db`, `dL/dx`
3. **Tanh activation** — local gradient and chain rule
4. **Batch Normalization** — one of the trickier ones; includes a digression on Bessel's correction
5. **1st Linear Layer** — same as above
6. **Embedding Table** — gradient scatter back into the embedding matrix

---

## 📝 Exercises

The notebook is structured around 4 progressive exercises:

| # | Exercise |
|---|----------|
| 1 | Backprop through the atomic compute graph (step by step) |
| 2 | Cross entropy loss — efficient backward pass |
| 3 | Batch norm layer — efficient backward pass |
| 4 | Putting it all together into a clean, manual `backward()` |

> ⚠️ **Karpathy's note:** *"I recommend you work through the exercise yourself but work with it in tandem and whenever you are stuck unpause the video and see me give away the answer. This video is not super intended to be simply watched."*

---

## 🔗 Resources

| Resource | Link |
|----------|------|
| 📹 YouTube Lecture | [Watch on YouTube](https://www.youtube.com/watch?v=q8SA3rM6ckI) |
| 📓 Exercise Notebook (Colab) | [Open in Colab](https://colab.research.google.com/drive/1WV2oi2fh9XXyldh02wupFQX0wh5ZC-z-?usp=sharing) |
| 🗂️ Full Series Playlist | [Neural Networks: Zero to Hero](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) |

---

## 🧱 Prerequisites

You should be comfortable with:

- **Part 3** — Activations, Gradients & BatchNorm ([YouTube](https://www.youtube.com/watch?v=P6sfmUTpUmc))
- Basic calculus (chain rule, partial derivatives)
- PyTorch tensors and operations

---

## 🛠️ Setup

```bash
pip install torch matplotlib
```

The notebook uses:
- `torch` — tensor operations and gradient checking
- `matplotlib` — visualizing activation/gradient distributions

---

## 💡 Key Takeaways

- Manual backprop forces you to understand **exactly** what autograd does under the hood.
- Batch normalization's backward pass is non-trivial — working through it manually is very clarifying.
- After this, you'll be much more confident reading and debugging modern neural network code.
- Gradient checking with `torch.allclose()` against autograd is used throughout to verify correctness.

---

## 📂 Series Navigation

| Part | Topic |
|------|-------|
| Part 1 | [Bigram Language Model](https://www.youtube.com/watch?v=PaCmpygFfXo) |
| Part 2 | [MLP](https://www.youtube.com/watch?v=TCH_1BHY58I) |
| Part 3 | [Activations, Gradients & BatchNorm](https://www.youtube.com/watch?v=P6sfmUTpUmc) |
| **Part 4** | **Becoming a Backprop Ninja** ← you are here |
| Part 5 | [WaveNet](https://www.youtube.com/watch?v=t3YJ5hKiMQ0) |

---

*Based on Andrej Karpathy's [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) — highly recommended for anyone learning deep learning from first principles.*
