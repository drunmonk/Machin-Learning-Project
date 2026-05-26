# MicroGPT From Scratch 🚀

A minimal Transformer-based character-level language model built with PyTorch.

This project implements a simplified GPT-style architecture from scratch, including:

- Self Attention
- Multi-Head Attention
- Feed Forward Networks
- Transformer Blocks
- Positional Embeddings
- Autoregressive Text Generation

Inspired by Andrej Karpathy's nanoGPT tutorials.

---

# Features ✨

- Character-level language modeling
- Transformer decoder architecture
- Multi-head causal self-attention
- Text generation
- GPU support (CUDA)
- Dropout regularization
- Clean and beginner-friendly implementation

---

# Project Structure 📂

```bash
.
├── model.py
├── more.txt
├── README.md
└── requirements.txt
```

---

# Requirements 📦

Install dependencies:

```bash
pip install torch
```

Or install using requirements:

```bash
pip install -r requirements.txt
```

---

# Dataset 📖

The model trains on a plain text dataset.

Example:

```txt
more.txt
```

You can replace it with:

- Shakespeare text
- Novels
- Chat logs
- Poems
- Custom datasets

---

# Hyperparameters ⚙️

```python
batch_size = 32
block_size = 8
max_iters = 5000
learning_rate = 1e-2
n_embd = 32
dropout = 0.2
```

---

# Architecture 🧠

The model contains:

## 1. Token Embeddings

Converts characters into dense vectors.

## 2. Positional Embeddings

Adds sequence position information.

## 3. Self Attention Head

Learns relationships between tokens.

## 4. Multi Head Attention

Combines multiple attention heads.

## 5. Feed Forward Network

Adds non-linearity and deeper learning capacity.

## 6. Transformer Blocks

Stacked attention + feedforward layers.

## 7. Language Modeling Head

Predicts the next character.

---

# Training 🚂

Run:

```bash
python model.py
```

Training output:

```bash
step 0: train loss 4.21, val loss 4.19
step 300: train loss 2.45, val loss 2.51
...
```

---

# Text Generation ✨

After training, the model generates text character-by-character.

Example:

```txt
ROMEO:
What shall I do now?
```

# How Attention Works 🧩

The attention mechanism computes:

```text
Attention(Q, K, V) = softmax(QKᵀ / √d)V
```

This allows tokens to attend to previous tokens in the sequence.

---

# Model Flow 🔄

```text
Input Tokens
      ↓
Token Embedding
      ↓
Position Embedding
      ↓
Transformer Blocks
      ↓
LayerNorm
      ↓
Linear Head
      ↓
Next Token Prediction
```

---

# Example Generated Output 📝

```txt
KING:
Where are you going tonight?

JULIET:
I cannot stay here anymore.
```

---

# Future Improvements 🚀

- Increase context length
- Add LayerNorm before attention
- Use Flash Attention
- Add tokenizer support
- Train on larger datasets
- Implement GPT-2 architecture
- Add checkpoint saving/loading
- Mixed precision training
- Better sampling strategies

---

# Concepts Learned 📚

This project helps understand:

- Transformers
- Attention Mechanisms
- GPT Architecture
- Language Modeling
- Deep Learning with PyTorch
- Autoregressive Generation

---

# References 🔗

- Attention Is All You Need
- nanoGPT by Andrej Karpathy
- PyTorch Documentation

---

# License 📜

MIT License

---

# Author 👨‍💻

Built with PyTorch and Transformers.
