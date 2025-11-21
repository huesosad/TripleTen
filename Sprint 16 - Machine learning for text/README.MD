# Automated Sentiment Analysis for Movie Reviews | Project 16 - Tripleten
This project was part of my Data Scientist bootcamp at Tripleten

## Introduction
The Film Junky Union, an engaging community for classic movie enthusiasts, has embarked on a project to develop a system for filtering and categorizing movie reviews. They are interested in training a model capable of automatically identifying negative reviews. The task involved the use of an IMDb movie reviews dataset, which had been labeled according to sentiment polarity. The aim was to construct a model capable of classifying reviews as positive or negative with an F1 score of at least 0.85.

## Tasks
### 1 Data Preparation
Preprocessing involved techniques of data preparation as removal of unwanted characters, lower casing, tokenization, and lemmatization.

### 2. EDA (Exploratory Data Analysis)
EDA was conducted to understand the distribution of classes in the data, which revealed a class imbalance. This understanding was crucial as it guided the choice of metrics for model evaluation and strategies for handling the class imbalance during model training.

The data was further preprocessed to prepare it for modeling. This involved transforming the text data into numerical representations that can be understood by machine learning algorithms, using techniques such as Bag-of-Words or TF-IDF.

### 3. Model Training and Testing
4 different models were trained: (F1 score in test set)
- Model 0: Baseline (Logistic Regression) | F1 score: 0, CPU time: 1s
- Model 1: NLTK, TF-IDF (Logistic Regression) | F1 score: 0.88, CPU time: 3.83s
- Model 2: spaCy, TF-IDF (Logistic Regression) | F1 score: 0.88, CPU time: 4.05s
- Model 3: spaCy, TF-IDF (LGBMClassifier) | F1 score: 0.86, CPU time: 1min 32s
- Model 4: BERT (Logistic Regression) | F1 score: 0.86, CPU time: 4min 29s

The trained models were then tested on a set of newly composed reviews. Differences in the testing results of the models were observed and interpreted.

### 4. Conclusions

All the models achieved an F1 score above 0.85, which is a strong result overall. However, the time each model requires varies significantly. After reviewing the predictions manually with a “human eye,” we observed the following:

Model 1 produced 2 misclassified reviews.

Model 2 produced 1 misclassified review and another that fell right in the middle.

Model 3 produced 1 misclassified review.

Model 4 (BERT) generated predictions that skew more toward the extremes (closer to 0 and 1) and resulted in 1 misclassified review.

Based on these results, I would recommend that Film Junky Union use Model 3, which is the combination of spaCy, TF-IDF, and LGBMClassifier. If additional computational resources are available, BERT with Logistic Regression is also a strong option, especially considering that BERT captures significantly more contextual information from the entire corpus.
