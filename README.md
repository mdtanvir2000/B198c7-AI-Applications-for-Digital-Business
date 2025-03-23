

# AI Applications for Digital Business - Sentiment Analysis

## Project Overview

This project aims to develop an **AI application** to perform **sentiment analysis** on tweets. The goal is to classify tweets as **positive**, **negative**, or **neutral** based on their content. This solution can be applied in fields like **marketing**, **customer service**, or **brand management** to understand customer opinions and enhance decision-making processes.

---

## Table of Contents
1. [Business Problem](#business-problem)
2. [Data Preprocessing](#data-preprocessing)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Feature Engineering](#feature-engineering)
5. [Model Training and Evaluation](#model-training-and-evaluation)
6. [Results and Discussion](#results-and-discussion)
   
---

## Business Problem

The business problem addressed in this project is to automatically classify the sentiment of customer tweets into positive, negative, and neutral categories. This will help businesses:
- **Identify customer sentiment**: Understand how customers feel about a product or service.
- **Improve marketing strategies**: Tailor marketing messages based on customer sentiments.
- **Enhance customer service**: Prioritize addressing negative sentiment to improve customer satisfaction.

---

## Data Preprocessing

The dataset used in this project is a collection of **tweets** with sentiment labels. The preprocessing steps involved:
1. **Cleaning the Data**: Removed unnecessary columns (timestamps, usernames, etc.) and cleaned the text data by:
   - Removing URLs and mentions (@username).
   - Removing non-alphabetic characters.
   - Converting text to lowercase.
2. **Text Tokenization**: Splitting the cleaned text into individual words.
3. **Stopword Removal**: Removing common English words like "the", "is", "and", etc., that don’t contribute much meaning.

---

## Exploratory Data Analysis (EDA)

In the exploratory phase, several visualizations were generated to understand the dataset:
1. **Sentiment Distribution**: A count plot to show the frequency of positive, negative, and neutral tweets.
2. **Tweet Length Distribution**: A histogram to visualize the distribution of tweet lengths.
3. **Word Cloud**: A word cloud to visualize the most frequent words in the dataset.
4. **Sentiment vs. Tweet Length**: A box plot to compare tweet lengths across different sentiment classes.
5. **Most Common Words in Positive and Negative Sentiments**: Bar plots to highlight the most common words in positive and negative tweets.

---

## Feature Engineering

For feature engineering, we used **TF-IDF Vectorization** to convert the cleaned tweet text into numerical features that can be fed into machine learning models:
- **TF-IDF (Term Frequency-Inverse Document Frequency)** was used to capture the importance of words in the tweets relative to the entire corpus.

The feature matrix was created using the top 5000 most significant words.

---

## Model Training and Evaluation

### Model Selection:
The following models were used:
- **Logistic Regression**: Initially trained to perform sentiment classification.

### Evaluation Metrics:
- **Accuracy**: To measure the percentage of correct classifications.
- **Precision, Recall, F1-Score**: To evaluate model performance across different sentiment classes.
- **Confusion Matrix**: To visualize true positives, false positives, true negatives, and false negatives.
- **ROC Curve and AUC**: To assess the model's ability to discriminate between classes.

### Hyperparameter Tuning:
- Used **GridSearchCV** to optimize hyperparameters such as the regularization strength (`C`) for Logistic Regression.

---

