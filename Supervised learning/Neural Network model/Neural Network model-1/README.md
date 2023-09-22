# Neural Network Model Example

This repository contains a Python script that demonstrates how to implement a basic neural network model for image classification using preloaded weights. The code uses the NumPy library for numerical operations, Matplotlib for data visualization, and SciPy for loading external data files.

## Purpose

The main purpose of this code is to provide a clear and simple example of how to build a neural network model and make predictions using pre-trained weights. The emphasis here is on understanding the structure of the neural network and its basic functionality rather than fine-tuning or optimizing the model. 

## Code Explanation

### Data Loading
- The script loads pre-trained neural network weights from 'ex3weights.mat' using SciPy.
- It also loads image data from 'ex3data1.mat', which will be used for prediction.

### Data Display
- The `display_data` function is used to display a grid of images from the dataset.
- The `display_example` function displays a single image from the dataset.

### Neural Network Model
- The neural network has two layers (input and output).
- The `model` function computes predictions using the preloaded weights and the sigmoid activation function.
- The `predict` function transforms the model's output into a human-readable prediction.

### Evaluation
- The code evaluates the model's predictions against the ground truth labels and calculates the percentage of correct predictions.

## Usage

To run the code, make sure you have Python and the required libraries (NumPy, Matplotlib, and SciPy) installed. You can then execute the script by running the jupyter notebook

## Acknowledgments
- The preloaded weights and dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes 