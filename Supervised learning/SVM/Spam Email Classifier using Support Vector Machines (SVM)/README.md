# Spam Email Classifier using Support Vector Machines (SVM)

## Overview
This project is designed as an educational resource for beginners and demonstrates the implementation of a spam email classifier using Support Vector Machines (SVM). The classifier's purpose is to determine whether an email is spam or not based on its content. The project utilizes Python and various libraries for text preprocessing, feature extraction, and machine learning.

## Modules Used
The following Python modules are used in this project:

- `numpy` and `matplotlib.pyplot`: These libraries are used for numerical computations and data visualization, respectively.

- `scipy.io`: The `scipy.io` library is used to load MATLAB files containing the training and test datasets.

- `sklearn.svm.SVC`: The `SVC` class from the `sklearn.svm` module is used to create and train the Support Vector Machine classifier.

- `nltk`: The Natural Language Toolkit (NLTK) is a library used for natural language processing tasks. In this project, we use it to perform stemming of words.

- `re`: The `re` module is used for regular expressions to perform text cleaning and processing.

## Project Description
The main components of this project include:

### 1. Loading the Dataset
The project starts by loading a pre-existing dataset of emails. The dataset is stored in a MATLAB file format, and the `scipy.io` library is used to load it into Python.

### 2. Text Preprocessing
The emails in the dataset undergo extensive text preprocessing to prepare them for feature extraction. This includes:

- Removing HTML tags from the emails.
- Replacing URLs with a generic "httpaddr" token.
- Replacing email addresses with an "emailaddr" token.
- Replacing numbers with a "number" token.
- Replacing dollar signs with a "dollar" token.
- Removing punctuation and extra white spaces.
- Stemming words to their base form using NLTK's Porter Stemmer.

### 3. Feature Vectorization
Each preprocessed email is transformed into a feature vector. This is done by comparing the words in the email against a vocabulary of the top 1899 words found in spam emails. If a word from the email is present in the vocabulary, the corresponding element in the feature vector is set to 1; otherwise, it remains 0.

### 4. Training the SVM Classifier
A Support Vector Machine (SVM) classifier with a radial basis function (RBF) kernel is used. The model is trained using the feature vectors obtained from the training dataset.

### 5. Model Evaluation
The performance of the trained SVM classifier is evaluated on both the training and test datasets. The accuracy of the classifier on these datasets is calculated and reported.

### 6. Email Classification
Finally, the SVM classifier is used to predict whether a new email is spam or not based on its feature vector. The project provides a simple "spam" or "not spam" prediction for a sample email.

## Running the Code
To run this project, follow these steps:

1. Make sure you have Python and the required libraries (NumPy, Matplotlib, SciPy, NLTK, scikit-learn) installed.
2. Download the project files, including the spam training and test datasets.
3. Run the code in your Python environment, ensuring that all paths to dataset files are correctly specified.
4. The code will preprocess the emails, train the SVM classifier, and evaluate its performance on the datasets. It will also classify a sample email as spam or not spam.

## Conclusion
This project provides an introduction to text classification using Support Vector Machines and demonstrates the essential steps involved in building a spam email classifier. It is a beginner-friendly project that showcases text preprocessing, feature engineering, and machine learning in a practical context. Feel free to explore and modify the code to enhance your understanding of text classification and machine learning techniques.

## Acknowledgments
- The preloaded dataset are part of the "Machine Learning" course on Coursera by Stanford University.
- This code serves as a simplified example for educational purposes
