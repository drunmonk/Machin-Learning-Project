# Earthquake Magnitude Classification Project - Part 1

This is the first part of the Earthquake Magnitude Classification project, which aims to classify earthquake magnitudes into three classes: low, medium, and high. The project involves labeling earthquake data and creating a super dataset by combining multiple datasets to address class imbalance. Additionally, this project includes machine learning to search for hidden patterns that can potentially be exploited to deal with future earthquakes effectively.

## Objective

The objective of this part of the project is to prepare the data for the earthquake magnitude classification task. This involves the following steps:

1. Labeling the Data: The raw earthquake data is preprocessed, and magnitude values are rounded and classified into three classes: low, medium, and high.

2. Data Analysis: Exploratory data analysis (EDA) is performed on the earthquake datasets to search for any hidden patterns, trends, or correlations that may exist between earthquake magnitudes and their geographical locations.

3. Super Dataset Creation: To address class imbalance, nine datasets are superimposed, containing earthquakes from different sources, and class distribution is balanced.

## Code Description

The `Earthquake_Magnitude_Classification_Project_part-1.ipynb` Jupyter notebook contains the Python code for this part of the project. It performs the following tasks:

1. Reads and preprocesses the data from the above datasets.
2. Rounds the earthquake magnitudes and classifies them into low, medium, and high classes.
3. Conducts data analysis using visualizations and statistical methods to explore hidden patterns.
4. Creates a super dataset by merging and balancing the class distribution from the nine datasets.
5. Exports the final super dataset to a CSV file named `superearthquakedataset.csv`.

## Usage

To reproduce the results of this part of the project, follow these steps:

1. Clone the entire repository to your local machine.
2. Open the `Earthquake_Magnitude_Classification_Project_part-1.ipynb` notebook in Google Colab or any Jupyter environment that supports Python 3 and pandas.
3. Execute each code cell in the notebook sequentially to label the data, conduct data analysis, and create the super dataset.
4. The resulting `superearthquakedataset.csv` file will be available for download at the end of the notebook.

## Data Analysis

EDA techniques are applied to the earthquake datasets to gain insights into earthquake magnitudes and their spatial distribution. This analysis aims to identify potential patterns or relationships that could help in understanding and predicting earthquake occurrences in the future.

## Super Dataset Creation

The super dataset is created by combining earthquakes from the nine datasets, ensuring a balanced distribution of low, medium, and high-magnitude earthquakes.

## Conclusion

This part of the project prepares the data for the earthquake magnitude classification task . The resulting super dataset will be used in the next part of the project, where we will train and evaluate the earthquake magnitude classification model.

As we move forward with the project, we hope to gain valuable insights from the data analysis, which could potentially aid in developing effective strategies to deal with future earthquakes and enhance earthquake preparedness and response measures.


