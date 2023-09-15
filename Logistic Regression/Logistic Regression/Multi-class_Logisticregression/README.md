# Multi-Class Logistic Regression from Scratch - README

## Introduction

This project demonstrates the implementation of multi-class logistic regression from scratch using Python. Unlike binary logistic regression, this code is designed for multi-class classification tasks. The main goal of this project is to help beginners understand the fundamental workings of the multi-class logistic regression model. The code focuses on building the model rather than optimizing its performance.

## Code Explanation

### Modules Used

1. `numpy` - A powerful library for numerical computations in Python.
2. `matplotlib` - Used for data visualization, particularly for plotting graphs.
3. `scipy.io` - Provides tools for reading and writing MATLAB data files.
4. `random` - Python's built-in module for generating random numbers..

### Loading and Displaying Data

The code loads data from a MATLAB data file (`ex3data1.mat`) using the `scipy.io.loadmat` function. It also defines a function `display_data` to display a random subset of the dataset.

### Data Preprocessing

- The code initializes the feature matrix `X` with ones and copies the actual data into it.
- It creates the target matrix `Y` by tiling a base array and converting it to a suitable format.
- The target matrix `Y` is further converted to the form that the model outputs.

### Multi-Class Logistic Regression

The multi-class logistic regression model is built using the following functions:

- `sigmoid(z)`: A sigmoid function to model probabilities.
- `Costfunction(h, yt)`: The cost function for multi-class logistic regression.
- Gradient Descent: The code performs gradient descent to optimize the model's parameters (theta) based on the cost function.

### Hyperparameters and Training

- `alpha` and `num_iterations` are set as hyperparameters for training.
- The code stores the cost history during training and plots it to visualize the learning process.

### Model Evaluation

- The trained model is used to make predictions for multi-class classification.
- The percentage of correctly predicted elements is calculated and displayed.

## Project Focus

This project is designed to provide a basic understanding of multi-class logistic regression's inner workings. It intentionally prioritizes clarity over optimization and doesn't aim for high performance. It serves as a starting point for beginners to delve into machine learning and build a solid foundation in multi-class classification.

Feel free to explore and modify the code to experiment with different aspects of multi-class logistic regression.

# Acknowledgments
- The preloaded dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes
