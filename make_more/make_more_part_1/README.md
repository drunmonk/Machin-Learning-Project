# 🧠 Bigram Language Model (Andrej Karpathy Inspired) — Part 1

This repository contains my implementation of a **Bigram Language Model** built in a Jupyter Notebook, inspired by Andrej Karpathy’s deep learning tutorials.

## 📌 Overview

In this project, I follow along with Karpathy’s approach to understand how language models work at a fundamental level by building a simple **character-level bigram model** from scratch.

A **bigram model** predicts the next character based only on the previous one. While simple, it forms the foundation for understanding more advanced models like transformers.

---

## 🚀 What This Notebook Covers

* Loading and preprocessing text data
* Creating a character-level vocabulary
* Encoding and decoding text
* Building a bigram frequency table
* Converting counts to probabilities
* Sampling from the model to generate text
* Understanding the limitations of bigram models

---

## 🧰 Tech Stack

* Python 🐍
* Jupyter Notebook 📓
* PyTorch (optional, depending on implementation)

---

## 📂 File Structure

```
.
├── bigram_model.ipynb   # Main notebook
├── input.txt            # Training text dataset
└── README.md            # Project documentation
```

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/bigram-model.git
   cd bigram-model
   ```

2. Install dependencies:

   ```bash
   pip install torch numpy matplotlib
   ```

3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `bigram_model.ipynb` and run all cells.

---

## 💡 Example Output

The model generates text character by character. Since it's a simple bigram model, the output will look noisy but will still capture some structure from the training data.

Example:

```
thand he s an wome t ing, s to wathis...
```

---

## 📈 Key Learnings

* How probability drives text generation
* Why context matters in language models
* Limitations of simple statistical models
* Foundation for moving toward neural networks

---

## 🔜 What's Next

In future parts, I plan to:

* Improve the model using neural networks
* Introduce embeddings
* Move toward transformer-based architectures

---

## 🙌 Credits

Inspired by Andrej Karpathy’s amazing deep learning tutorials.

---

## 📜 License

This project is open-source and available under the MIT License.

---

⭐ If you found this helpful, consider giving the repo a star!
