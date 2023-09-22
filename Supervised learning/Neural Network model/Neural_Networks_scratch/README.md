# Neural Network Implementation with Backpropagation and Regularization

This is a simple neural network implementation with three layers (input, hidden, output) designed to help beginners understand how neural networks work under the hood. It includes code for loading data, forward and backward propagation, cost calculation, and training. The primary focus of this code is on education rather than model performance.

## Getting Started

To run this code and experiment with the neural network, you'll need Python 3 and the following libraries installed:

- NumPy
- Matplotlib
- SciPy

You can install these libraries using pip:


## Code Explanation

Here's a brief explanation of the code and its modules:

- `choice` Function: Generates random numbers to choose a random range of data for display.

- `display_data` Function: Visualizes the data as images.

- `forward_propagation` Function: Implements forward propagation to compute layer activations.

- `sigmoid` Function: Computes the sigmoid activation function.

- `Costfunction` Function: Computes the cost function for binary classification.

- `RegCostfunction` Function: Computes the regularized cost function to prevent overfitting.

- `sigmoidGradient` Function: Computes the gradient of the sigmoid function for backpropagation.

- `randInitializeWeights` Function: Initializes neural network weights randomly to break symmetry.

- `gradeint` Function: Computes gradients of neural network parameters using backpropagation.

- `computeNumericalGradient` Function: Computes numerical gradients for debugging.

- `training` Function: Trains the model to find optimal weights using gradient descent.

- `Plotting`: Visualizes the cost function over iterations.

- `Prediction`: Uses the trained model to make predictions.

## Usage

1. Load and preprocess your data. Ensure your data is compatible with the code's input format.

2. Set hyperparameters such as learning rate (alpha), regularization parameter (lm), and the number of training iterations (num_iterations).

3. Initialize the neural network weights using `randInitializeWeights`.

4. Train the neural network using the `training` function, passing your data and hyperparameters.

5. Visualize the cost function over training iterations to assess training progress.

6. Make predictions using the trained model and evaluate its performance.

## Note

This code is designed for educational purposes and may not yield state-of-the-art performance. It serves as a foundation for understanding neural networks and can be a starting point for building more complex models.

Feel free to experiment with different hyperparameters and datasets to gain a deeper understanding of neural network training.

If you have any questions or encounter issues, please refer to the code comments or reach out for assistance.

Happy learning!

## Acknowledgments
- The preloaded  dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes

