# Logistic Regression Example: Understanding Logistic Regression from Scratch

This project provides a step-by-step implementation of logistic regression from scratch using Python. The code demonstrates how logistic regression works and includes explanations for each major component. This is designed to help beginners understand the fundamental concepts behind logistic regression and its implementation.

## Libraries Used

The following libraries are used in this project:

- **NumPy**: A powerful library for numerical computations in Python. It provides support for large, multi-dimensional arrays and matrices, along with various mathematical functions to operate on these arrays.

- **Matplotlib**: A widely used plotting library in Python. It allows you to create a variety of plots and visualizations to understand and present data.

## Code Explanation

1. **Data Loading and Preparation**: The project starts by loading data from a CSV file (`ex2data1.txt`). The data is assumed to be in a comma-separated format. The code initializes variables (`x1`, `x2`, and `y`) to hold the features and labels. It also uses Matplotlib to create a scatter plot of the data points, distinguishing between two classes using different markers and colors.

2. **Feature Scaling and Data Preparation**: The features are normalized to improve convergence during gradient descent. The mean normalization is applied to the feature matrix, excluding the first column of ones.

3. **Gradient Descent**: The core of logistic regression is implemented here. A sigmoid function is used to model the probability of a sample belonging to a specific class. The cost function, gradient, and parameter updates are calculated using NumPy operations. Gradient descent is performed to minimize the cost.

4. **Cost Function and Sigmoid Function**: The `sigmoid` function models the sigmoid curve to predict probabilities. The `Costfunction` function calculates the cost of the predicted probabilities compared to the actual labels.

5. **Plotting the Cost Function**: The cost function's value is plotted over iterations to visualize the convergence of gradient descent.

6. **Making Predictions and Calculating Accuracy**: After learning the parameters (`theta`) through gradient descent, predictions are made on the training data. The predicted probabilities are converted to binary labels (0 or 1) using a threshold of 0.5. The accuracy of the model is calculated by comparing the predicted labels with the actual labels.

7. **Plotting the Decision Boundary**: The decision boundary is calculated based on the learned parameters and then plotted along with the data points.

8. **Prediction Example**: An example of how to use the trained model for making predictions on new data is provided. The input values are scaled using the same normalization factors as the training data. The predicted probability of admission is calculated and displayed.

## How to Use

1. Make sure you have the required libraries (`NumPy` and `Matplotlib`) installed. You can install them using `pip`:

   ```shell
   pip install numpy matplotlib
2. Download the ex2data1.txt file and place it in the same directory as the code.

3. Run the code (logistic_regression_from_scratch.py).

4. The code will load the data, perform logistic regression, and display plots illustrating the process.

5.  Feel free to modify the hyperparameters (alpha and num_iterations) and observe their effects on the results

## Conclusion
This project offers an educational walkthrough of implementing logistic regression from scratch using Python and NumPy. By following the code and explanations provided, beginners can gain a deeper understanding of how logistic regression works and how to build a basic machine learning model without relying on external libraries.

Feel free to use this project as a learning resource to explore the mechanics of logistic regression and its role in classification tasks.