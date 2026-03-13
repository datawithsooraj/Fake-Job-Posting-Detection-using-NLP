# Fake-Job-Posting-Detection-using-NLP

## Project Overview

The rapid growth of online job portals has made job searching easier, but has also increased the number of fraudulent job postings. These fake job listings can mislead job seekers, waste time, and sometimes lead to financial loss or identity theft.

This project builds a machine learning model using Natural Language Processing (NLP) to automatically classify job postings as real or fraudulent.

## Dataset

### Dataset Source: Kaggle – Fake Job Postings Dataset

Dataset Characteristics:

Feature	Description
Total records	~17,880
Total features	18
Target variable	fraudulent
Real jobs	0
Fake jobs	1

## Data Preprocessing

### The following preprocessing steps were applied:

• Removed columns with excessive missing values
• Handled missing data in categorical and text features
• Combined multiple text fields into a single feature
• Converted text to lowercase
• Removed special characters and numbers
• Removed stopwords
• Applied lemmatisation

## Feature Engineering
### TF-IDF Vectorization

Text data was transformed into numerical features using TF-IDF (Term Frequency–Inverse Document Frequency).

Benefits of TF-IDF:

• Captures important words in job descriptions
• Reduces the impact of common words
• Improves classification performance

Parameters used:
• max_features = 5000
• ngram_range = (1,2)

## Model Architecture

A Deep Neural Network was implemented using TensorFlow/Keras.

Architecture:

Input Layer
↓
Dense Layer (ReLU)
↓
Dropout Layer
↓
Dense Layer
↓
Dropout
↓
Output Layer (Sigmoid)

Activation Functions:

- ReLU (hidden layers)
- Sigmoid (binary classification output)


## Model Evaluation

The model was evaluated using:

1. Accuracy
2. Precision
3. Recall
4. Confusion Matrix
5. ROC-AUC Score

These metrics help measure how effectively the model detects fraudulent job postings.

## Results

The model achieved strong performance in distinguishing between real and fake job postings.

- Accuracy: 97%
- ROC-AUC Score: 0.98
