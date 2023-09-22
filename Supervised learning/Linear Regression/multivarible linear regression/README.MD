# Multivariable Linear Regression from Scratch

This project is a demonstration of how to implement a multivariable linear regression model from scratch using Python. The goal is to provide beginners with a step-by-step explanation of the key concepts involved in building a multivariable linear regression model.

## Code Explanation

The code in this repository consists of two parts:

1. **Gradient Descent Implementation**: The first part of the code showcases how to implement gradient descent for multivariable linear regression. The dataset is loaded from a file (data.txt), and the input features are normalized and mean-centered. The gradient descent algorithm is used to learn the optimal coefficients (theta) that minimize the cost function. The code also plots the convergence of the cost function over iterations.

2. **Normal Equation Implementation**: The second part of the code demonstrates an alternative method for calculating the optimal coefficients (theta) using the normal equation. The dataset is loaded and transformed into a design matrix. The normal equation is used to find the exact solution for theta without requiring an iterative optimization algorithm.

## How to Use

1. Ensure you have Python and the required libraries (NumPy, Matplotlib) installed.

2. Place your dataset in a file named `data.txt` with each row containing space-separated values for input features and target values.

3. Run the code using a Python interpreter.

4. The code will output the learned coefficients (theta) and the final cost function value for the gradient descent implementation. It will also predict prices for a specific input using both gradient descent and the normal equation.

5. You can modify the parameters in the code, such as learning rate, number of iterations, and input features, to experiment with different settings.

## Dependencies

This project uses the following Python libraries:

- NumPy: Used for numerical operations and array manipulation.
- Matplotlib: Used for creating plots to visualize the convergence of the cost function.

## Purpose

The primary purpose of this project is educational. It aims to provide beginners with a clear understanding of how a multivariable linear regression model is built from scratch. The code includes comments explaining each step, making it accessible even to those new to programming and machine learning concepts.

Feel free to use, modify, and expand upon this code for your learning and experimentation. Happy coding!

