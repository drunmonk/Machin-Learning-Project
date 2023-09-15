# Regularization and Polynomial Logistic Regression

## Overview

This project focuses on building a polynomial logistic regression model and exploring the effects of the regularization parameter (lambda) on the model's performance. The primary goal is to demonstrate the impact of different lambda values on the decision boundary of the model rather than optimizing its performance.

## Code Explanation

### Modules Used

1. **NumPy**: NumPy is a Python library for numerical computations. It is used extensively for data manipulation and array operations.

2. **Matplotlib**: Matplotlib is a popular Python library for creating visualizations and plots. It is used to visualize the dataset and the decision boundary.

3. **scikit-learn (sklearn)**: scikit-learn is a machine learning library for Python. In this project, we use the `PolynomialFeatures` class from scikit-learn to create polynomial features for our dataset.

### Loading and Preprocessing the Data

- The project starts by loading data from the 'ex2data2.txt' file using NumPy. This data represents a classification problem with two features (microchip test1 and test2) and binary labels (admitted or not admitted).

- The dataset is then split into feature vectors `x1` and `x2`, as well as the target variable `y`.

### Data Visualization

- The data is visualized using Matplotlib. Scatter plots are created to distinguish between admitted and not admitted students based on their test scores.

### Polynomial Feature Generation

- Polynomial features are created using scikit-learn's `PolynomialFeatures` class. This step involves transforming the original feature matrix into one with additional polynomial features up to a specified degree (in this case, degree 6).

### Logistic Regression

- Logistic regression is implemented with regularization. The project defines functions for sigmoid activation, cost function computation, and gradient descent optimization.

- The optimization function (`optimization`) uses gradient descent to update the model parameters (theta) while considering regularization.

- Different values of lambda (regularization parameter) are used to train the model, and the cost function is plotted over iterations to visualize the convergence.

### Decision Boundary

- The project includes a function (`plot_decision_boundary`) to plot the decision boundary of the logistic regression model. This allows us to see how different lambda values affect the model's decision boundary.

### Running the Code

- The code can be executed by running the provided Python script. It contains three different runs with different lambda values: 0, 0.001, and 1.

- After running the code, you will see the cost function plots and decision boundaries for each lambda value.

## Conclusion

This project serves as an educational exploration of regularization and its impact on the decision boundary of a logistic regression model. It demonstrates how different lambda values can lead to different levels of model complexity and overfitting. Remember that the primary focus here is to understand the effects of lambda rather than optimizing the model's performance for practical use.

## Acknowledgments
- The preloaded weights and dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes 
