# Movie Recommendation System with Collaborative Filtering

## Overview

This project is a simple implementation of a movie recommendation system using collaborative filtering. It is aimed at beginners to help them understand the fundamental concepts behind collaborative filtering and recommendation systems.

Collaborative filtering is a technique used in recommendation systems to provide personalized recommendations based on user behavior and preferences. In this project, we'll walk through the steps of building a movie recommendation system from scratch.

## Libraries Used

This project makes use of the following libraries:

- `numpy`: Used for numerical computations, matrix operations, and random initialization of weights.

- `matplotlib`: Used for plotting graphs and visualizing the cost function over iterations.

- `scipy.io`: Used for loading data from `.mat` files.

## How It Works

### Data Loading and Preparation

We start by loading movie ratings data from a `.mat` file. The dataset includes user ratings for movies. We also add some example user ratings to demonstrate the recommendation system.

### Collaborative Filtering

1. **Cost Function (`cost`)**: We define a cost function to measure the accuracy of our predictions. It calculates the error between our predicted ratings and the actual ratings provided by users. Regularization terms are added to prevent overfitting.

2. **Gradient Descent (`gradient`)**: We implement the gradient descent algorithm to minimize the cost function. It updates the user and movie feature matrices (`X` and `Theta`) to improve our predictions.

3. **Training (`train`)**: We train the collaborative filtering model using gradient descent. It iteratively updates the feature matrices to optimize our predictions. We monitor the cost function to ensure it decreases with each iteration.

### Normalizing Ratings

We normalize user ratings to handle missing ratings and variations in rating scales. This helps improve the accuracy of our recommendations.

### Making Recommendations

We make movie recommendations based on the learned feature matrices. The top-rated movies are selected and presented as recommendations to the user.

### Visualization

We plot the cost function over iterations to visualize the training progress and ensure convergence.

### Loading Movie List

We load a list of movie names from a text file to provide meaningful movie recommendations.

## Usage

1. Ensure you have the required libraries (`numpy`, `matplotlib`, and `scipy.io`) installed.

2. Load your movie ratings data from a `.mat` file (you can modify the file path in the code).

3. Customize your own ratings (if desired) to see personalized recommendations.

4. Run the code and follow the instructions to see movie recommendations.

## Acknowledgments
- The preloaded  dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes

## Conclusion

Collaborative filtering is a powerful technique used in recommendation systems to provide personalized suggestions to users. This project serves as a beginner-friendly introduction to collaborative filtering and movie recommendation systems.

Feel free to explore the code, experiment with different datasets, and further enhance the recommendation system.

Happy coding!