# Amazon Product Review Sentiment Analysis

## Introduction
Data obtained from [Kaggle](https://www.kaggle.com/datasets/tarkkaanko/amazon)
This repository contains a comprehensive analysis of customer review data for a product listed on Amazon. The main objective is to perform sentiment analysis on customer reviews to gain insights into their sentiments towards the product. The project utilizes natural language processing (NLP) techniques and machine learning models to accurately predict the sentiment of reviews.

## Dataset and Preprocessing
The dataset used in this analysis contains a collection of customer reviews for the selected product on Amazon. The raw data is subjected to data cleaning, where missing values are handled, and text preprocessing techniques are applied. The text is transformed to lowercase, special characters are removed, and words are stemmed to their base forms to ensure consistency and reduce noise in the data.

## Exploratory Data Analysis
Before diving into the modeling process, the cleaned data is explored through visualizations and statistical summaries. This step allows us to understand the distribution of sentiments in the dataset, identify any patterns or trends, and gain valuable insights that may influence the modeling approach.

## Vectorization and Feature Engineering
To build predictive models, the text reviews are converted into numerical representations. This process, known as vectorization, includes techniques like Count Vector and TF-IDF (Term Frequency-Inverse Document Frequency). The sentiment labels are encoded to numeric values for classification.

## Model Selection and Training
Multiple machine learning models are explored in this analysis, including Naive Bayes, Logistic Regression, and Support Vector Machines (SVM). Each model is trained on the training set and evaluated using the validation set. Performance metrics like accuracy, precision, recall, and F1 score are used to assess the models' effectiveness.


## Results
The trained models are then tested on a separate test set to assess their performance on unseen data. The confusion matrix is used to visualize the performance of the models, providing a detailed breakdown of correct and incorrect predictions for each sentiment class.

The final analysis offers insights into the sentiment trends of customers and identifies the most effective models for sentiment prediction in the context of the given product reviews on Amazon.

Please refer to the notebook files for detailed code and step-by-step implementation of the analysis.

Feel free to explore the repository; any feedback or contributions are greatly appreciated!
