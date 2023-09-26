# K-means Clustering from Scratch

This project aims to provide a hands-on understanding of how the K-means clustering algorithm works by building a simple implementation from scratch in Python. K-means is a widely used unsupervised machine learning algorithm used for data clustering.

## Project Overview

In this project, we implement a basic version of the K-means algorithm using Python and popular scientific libraries such as NumPy, Matplotlib, and SciPy. The code provided in this project performs the following tasks:

1. **Data Loading and Visualization**:
   - Loads a dataset containing data points (assumed to be stored in a dictionary called `data`).
   - Visualizes the data points using a scatter plot.

2. **K-means Algorithm**:
   - Defines two essential functions for K-means clustering:
     - `findClosestCentroids(centroid, data)`: Assigns each data point to its nearest centroid.
     - `computeCentroids(idx, data, k)`: Computes new centroids based on the assigned clusters.
   - Iteratively applies the above functions to cluster the data.

3. **Plotting**:
   - Provides a function for plotting clusters and centroid movement throughout the iterations.

4. **Main Modeling**:
   - Implements the core K-means modeling function that iteratively updates clusters and centroids.
   - Stores the centroid history for visualization.

5. **Visualization**:
   - Defines a function to visualize clusters and centroid history.

## Dependencies

This project relies on the following Python libraries:

- [NumPy](https://numpy.org/): For numerical operations and array handling.
- [Matplotlib](https://matplotlib.org/): For data visualization.
- [SciPy](https://www.scipy.org/): For scientific and mathematical functions.

## Usage

1. Ensure you have the required libraries (NumPy, Matplotlib, and SciPy) installed. You can install them using pip:
   pip install numpy matplotlib scipy

2. choose your dataset`. Modify the `x_example` assignment according to your dataset structure.

3. Configure the initial centroids, number of clusters (k), and maximum iterations in the script.

4. Run the script:python kmeans.py

5. The script will display a visualization of data points, clusters, and centroid movements throughout the iterations.

## Example

To demonstrate the K-means clustering, the code uses a simple example dataset. You can replace it with your own dataset as needed.

## Acknowledgments
- The preloaded  dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes


