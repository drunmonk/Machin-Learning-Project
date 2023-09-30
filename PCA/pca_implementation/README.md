# Principal Component Analysis (PCA) with 2D Data 

This repository contains a Python code example to demonstrate Principal Component Analysis (PCA) using a 2D dataset. PCA is a dimensionality reduction technique that is often used in data analysis and machine learning. The purpose of this example is to help beginners understand how PCA works using a simple and easy-to-visualize 2D dataset.

## Introduction

PCA is a statistical technique that simplifies the complexity in the high-dimensional data while retaining trends and patterns. It does this by transforming the original features into a new set of orthogonal (uncorrelated) features called principal components. These principal components are ranked by their ability to explain the variance in the data.

## Code Explanation

The code in this repository demonstrates the following steps:

1. **Data Normalization**: The dataset is first normalized to have a mean of zero and a standard deviation of one. This step ensures that all features are on the same scale.

2. **Covariance Matrix**: The covariance matrix of the normalized data is computed. The covariance matrix represents the relationships between the different features.

3. **Singular Value Decomposition (SVD)**: The code performs Singular Value Decomposition on the covariance matrix to find the principal components.

4. **Projection**: The data is projected onto the first principal component to reduce its dimensionality.

5. **Reconstruction**: The reduced-dimension data is then reconstructed back into the original feature space.

6. **Visualization**: The code includes visualization of the original data, the first and second principal components, and the projected and reconstructed data.

## Modules Used

The code uses the following Python libraries:

- **NumPy**: NumPy is used for numerical operations and array manipulations.

- **Matplotlib**: Matplotlib is used for data visualization, including creating scatter plots and line plots.

- **SciPy**: SciPy is used to load data from a .mat file, which is a common format for MATLAB data.

## Usage

To run this code, you should have Python and the required libraries (NumPy, Matplotlib, and SciPy) installed. Ensure that the 'ex7data1.mat' file is in the same directory as the code.

Run the code and observe how PCA reduces the dimensionality of the dataset while preserving important information.

## Conclusion

Principal Component Analysis (PCA) is a powerful technique for dimensionality reduction and data visualization. This example provides a simple and beginner-friendly demonstration of how PCA works using a 2D dataset, making it easier for newcomers to understand the concept.
## Acknowledgments
- The preloaded  dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes

Feel free to explore the code and modify it for your own datasets and experiments. Happy learning!

