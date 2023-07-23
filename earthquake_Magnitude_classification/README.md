# Earthquake Magnitude Classification Project

## Overview

The Earthquake Magnitude Classification Project aims to develop a machine learning model to classify earthquake magnitudes into three classes: low, medium, and high. The project is divided into two parts:

1. **Part 1: Data Exploration and Preparation**
   - In this part, we explore the earthquake data from various sources, conduct data analysis, and preprocess the data to prepare it for modeling.
   - We label the earthquake data based on magnitude and create a super dataset by combining multiple earthquake datasets to address class imbalance.
   - Additionally, we perform data analysis to search for hidden patterns or relationships between earthquake magnitudes and their geographical locations.

2. **Part 2: Modeling and Pattern Identification**
   - In the second part, we build a machine learning model to predict earthquake magnitudes based on historical earthquake data.
   - We use the Random Forest Classifier model to handle class imbalance effectively.
   - The goal is to develop a model that accurately classifies earthquake magnitudes, leveraging insights gained from data analysis in Part 1.

## Part 1: Data Exploration and Preparation

### Objective

The objective of Part 1 is to explore the earthquake data, conduct data analysis, and prepare the data for modeling. This part includes the following steps:

1. **Data Collection**: We gather earthquake data from different sources, such as Global Earthquake Data, Database Earthquake Data, and other relevant datasets.

2. **Data Preprocessing**: We preprocess the raw earthquake data by rounding magnitude values and classifying them into low, medium, and high-magnitude classes.

3. **Super Dataset Creation**: To handle class imbalance, we merge multiple earthquake datasets to create a balanced super dataset.

4. **Data Analysis**: Exploratory data analysis (EDA) techniques are applied to the data to search for hidden patterns, trends, or correlations between earthquake magnitudes and their geographical locations.

### Usage

To reproduce the results of Part 1, follow the instructions in the `Earthquake_Magnitude_Classification_Project_part-1.ipynb` Jupyter notebook. This notebook contains the Python code for data exploration, preprocessing, super dataset creation, and data analysis.

## Part 2: Modeling and Pattern Identification

### Objective

The objective of Part 2 is to develop a machine learning model that can accurately classify earthquake magnitudes based on historical earthquake data. This part includes the following steps:

1. **Model Selection**: We explore various machine learning techniques and algorithms, and based on the class imbalance issue, we choose the Random Forest Classifier model for its ability to handle imbalanced data.

2. **Model Training**: We train the Random Forest Classifier on the prepared super dataset from Part 1.

3. **Model Evaluation**: We evaluate the model's performance using appropriate metrics, such as accuracy, precision, and recall, to measure its effectiveness in classifying earthquake magnitudes.

4. **Pattern Identification**: Through model analysis, we aim to identify any underlying patterns or relationships in the earthquake data that contribute to accurate magnitude classification.

### Model Performance

The Random Forest Classifier model achieved an overall  score of 75%. This is a significant improvement (87% increase) compared to the previous models trained on raw data without labeling, highlighting the importance of data preparation and leveraging class balance for better model performance.

### Usage

To reproduce the results of Part 2, follow the instructions in the `Earthquake_Magnitude_Classification_Project_part-2.ipynb` Jupyter notebook. This notebook contains the Python code for model selection, training, evaluation, and pattern identification.

## Conclusion

The Earthquake Magnitude Classification Project is divided into two parts. Part 1 focuses on data exploration, preparation, and analysis, while Part 2 involves developing a Random Forest Classifier model to classify earthquake magnitudes and identifying hidden patterns.

By completing both parts of the project, we gained valuable insights into earthquake magnitude classification and successfully developed a robust model with improved performance compared to the previous attempts without proper data labeling.

As we move forward with the project, we hope to leverage the model's accuracy and identified patterns to deal with future earthquakes more effectively, enhancing earthquake preparedness and response measures.

Please note that this `README.md` file serves as an overview and guide for the Earthquake Magnitude Classification Project. For detailed instructions and code implementation, refer to the respective Jupyter notebooks.

## please note
The dataset used for this project is sourced from Kaggle. It was collected and curated by the original authors for research and analysis purposes. As responsible users of the data, we acknowledge and respect the efforts of the dataset authors and comply with any terms and conditions specified by them.
## Disclaimer

This project and the use of the dataset are for educational and research purposes only. The authors of this project do not claim any ownership or rights over the dataset. Any opinions, findings, and conclusions presented in this project are based on the analysis of the dataset and do not represent the views of the original dataset authors or Kaggle.

