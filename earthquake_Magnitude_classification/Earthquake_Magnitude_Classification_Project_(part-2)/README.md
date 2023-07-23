# Earthquake Magnitude Classification Project - Part 2

## Overview

Part 2 of the Earthquake Magnitude Classification Project focuses on training the data using the Random Forest Classifier model and evaluating its performance. The Random Forest Classifier is chosen due to its ability to handle class imbalance effectively and provide accurate predictions for earthquake magnitudes.

## Model Training and Evaluation

### Objective

The objective of Part 2 is to build a machine learning model using the Random Forest Classifier to predict earthquake magnitudes based on historical earthquake data. The steps include:

1. **Data Preprocessing**: We load the dataset created in Part 1, drop rows with missing values, and split the data into features (longitude and latitude) and the target variable (magnitude type, mag_type).

2. **Model Selection**: The Random Forest Classifier is selected for its ability to handle class imbalance and provide robust predictions for multi-class classification tasks.

3. **Model Training**: We train the Random Forest Classifier on the training data.
5. **Model Evaluation**: The trained model is evaluated on the test data to assess its performance.

### Model Performance

The Random Forest Classifier achieved the following performance metrics on the test set:

- Accuracy: 75.33%
- Precision: 75.07%
- Recall: 75.33%

The accuracy score represents the proportion of correctly classified earthquake magnitudes out of the total predictions. Precision measures the model's ability to correctly identify earthquake magnitudes of a specific class, while recall measures its ability to find all relevant instances of a particular class.

## Usage

To reproduce the results of Part 2, follow the instructions in the `Earthquake_Magnitude_Classification_Project_part-2.ipynb` Jupyter notebook. This notebook contains the Python code for data preprocessing, model training using the Random Forest Classifier, hyperparameter tuning, and model evaluation.

## Conclusion

Part 2 of the Earthquake Magnitude Classification Project successfully trained a Random Forest Classifier model to predict earthquake magnitudes based on geographical coordinates. The model's accuracy of 75.33% and balanced precision and recall scores demonstrate its effectiveness in classifying earthquake magnitudes into low, medium, and high categories.

With a well-trained machine learning model, we are better equipped to deal with future earthquakes by predicting their magnitudes accurately. The project's outcomes may contribute to improving earthquake preparedness and response measures for better safety and disaster management.

Please note that this `README.md` file provides an overview of Part 2 of the Earthquake Magnitude Classification Project. For in-depth code implementation and details, refer to the `Earthquake_Magnitude_Classification_Project_part-2.ipynb` Jupyter notebook.

