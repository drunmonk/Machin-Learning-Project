# Makemore Part 2 (MLP) — Notebook README

## 📌 Overview

This notebook is based on **Andrej Karpathy's Makemore Part 2: MLP lecture**, where we build a **Multi-Layer Perceptron (MLP)** from scratch to model character-level language generation.

The goal is to understand how neural networks can learn patterns in text data (such as names) and generate new, realistic samples.

---

## 🧠 What This Notebook Covers

* Building a character-level dataset
* Encoding characters into numerical representations
* Implementing an **embedding layer**
* Constructing a simple **MLP (Multi-Layer Perceptron)**
* Forward pass and loss computation
* Backpropagation and gradient updates
* Training loop and optimization
* Sampling new names from the trained model

---

## 📂 Dataset

The dataset typically consists of a list of names (e.g., `names.txt`).
Each name is treated as a sequence of characters, and the model learns to predict the next character given previous ones.

---

## ⚙️ Model Architecture

The model follows a simple pipeline:

1. **Input Context** (fixed-length sequence of characters)
2. **Embedding Layer**

   * Maps each character to a dense vector
3. **Hidden Layer**

   * Fully connected layer with non-linearity (e.g., `tanh`)
4. **Output Layer**

   * Produces logits for next-character prediction
5. **Softmax**

   * Converts logits into probabilities

---

## 🏗️ Key Concepts

* **Context Window**: Number of previous characters used for prediction
* **Embeddings**: Dense vector representations of characters
* **Activation Function**: Typically `tanh` in this notebook
* **Loss Function**: Cross-entropy loss
* **Gradient Descent**: Manual parameter updates

---

## 🚀 Training

The training loop involves:

* Forward pass
* Loss computation
* Backward pass (manual gradients or autograd)
* Parameter updates

Hyperparameters you may tune:

* Learning rate
* Embedding size
* Hidden layer size
* Batch size
* Number of iterations

---

## 🔍 Results

After training, the model should:

* Generate realistic-looking names
* Capture patterns like prefixes/suffixes
* Improve sample quality over time

---

## ✨ Sampling

You can generate new names by:

1. Starting with a special token (e.g., `.`)
2. Repeatedly sampling the next character
3. Stopping when an end token is produced

---

## 📦 Requirements

* Python 3.x
* PyTorch (or minimal tensor library)
* NumPy
* Matplotlib (optional, for visualization)

---

## 🧪 How to Run

1. Open the notebook:

   ```
   jupyter notebook makemore_mlp.ipynb
   ```
2. Run all cells sequentially
3. Observe training loss and generated samples

---

## 🎯 Learning Outcomes

By completing this notebook, you will:

* Understand how MLPs work internally
* Learn how embeddings represent discrete data
* Gain intuition for training neural networks from scratch
* Build a simple generative language model

---

## 📚 Reference

* Makemore Lecture Series by Andrej Karpathy
* Neural Networks: Zero to Hero

---

## 🛠️ Possible Improvements

* Add deeper networks
* Use ReLU instead of tanh
* Implement batch normalization
* Switch to more advanced architectures (RNNs, Transformers)

---

## 🙌 Acknowledgment

This work is inspired by the Makemore lecture series and is intended for educational purposes.

---

## 📄 License

This project is open-source and free to use for learning and experimentation.

---
