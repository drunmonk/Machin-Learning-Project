# Image Compression with K-Means Clustering

## Introduction

This project demonstrates the concept of image compression using the K-Means clustering algorithm. It aims to provide a beginner-friendly example of how K-Means clustering can be applied to reduce the size of an image while preserving its essential features. The code provided in this project utilizes Python and popular libraries such as NumPy, Matplotlib, and SciPy.

## Project Overview

### K-Means Clustering

K-Means clustering is an unsupervised machine learning algorithm used for partitioning data points into clusters based on their similarity. In this project, K-Means is employed to group pixels in an image into clusters, where each cluster is represented by its centroid. This allows us to replace multiple similar colors in the image with fewer representative colors, thereby reducing the image's size.

### Libraries Used

- **NumPy**: NumPy is a fundamental library for scientific computing in Python. It is used extensively for numerical operations and array manipulation in this project.

- **Matplotlib**: Matplotlib is a popular library for creating data visualizations. In this project, it is used for displaying the original and compressed images.

- **SciPy**: SciPy is a library for scientific and technical computing. It is used to load image data from a .mat file.

## Getting Started

To run this project, follow these steps:

1. Clone the repository to your local machine:


2. Install the required Python libraries if you haven't already:
  pip install numpy matplotlib scipy
3. Run the image_compression.py script

# How it Works

**Data Preparation**: The project loads an image (e.g., 'bird_small.mat') using SciPy and flattens it into a 2D array of RGB pixel values.

**K-Means Initialization**: It randomly initializes K centroids, where K is the desired number of colors in the compressed image.

**K-Means Clustering**: The K-Means clustering algorithm is applied to group pixel colors into K clusters. Each pixel is assigned to the nearest centroid, and centroids are recomputed based on the assigned pixels.

**Image Reconstruction**: The compressed image is reconstructed by replacing each pixel with the color of its assigned cluster's centroid.

**Visualization**: The original and compressed images are displayed side by side using Matplotlib.

# Conclusion

This project demonstrates a simple yet effective application of the K-Means clustering algorithm for image compression. It serves as a practical example for beginners to understand how clustering algorithms can be used to reduce the size of images while maintaining their visual quality.

## Acknowledgments
- The preloaded  dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes

Feel free to experiment with different images and values of K to observe the varying levels of compression and image quality.

Happy coding!
