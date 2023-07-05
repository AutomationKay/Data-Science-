# Amazon Product Review Sentiment Analysis
![44525-v3-600x](https://github.com/AutomationKay/Data-Science-/assets/112325655/eddf6e78-1c73-4833-8548-372f1bd8aec9)


## **Introduction**
Data obtained from [Kaggle](https://www.kaggle.com/datasets/tarkkaanko/amazon)


This repository contains a comprehensive analysis of customer review data for a product listed on Amazon. The main objective is to perform sentiment analysis on customer reviews to gain insights into their sentiments towards the product. The project utilizes natural language processing (NLP) techniques and machine learning models to accurately predict the sentiment of reviews.

## **Dataset and Preprocessing**
The dataset used in this analysis contains a collection of customer reviews for the selected product on Amazon. The raw data is subjected to data cleaning, where missing values are handled, and text preprocessing techniques are applied. The text is transformed to lowercase, special characters are removed, and words are stemmed to their base forms to ensure consistency and reduce noise in the data.
![piechart](https://github.com/AutomationKay/Data-Science-/assets/112325655/a31b5ade-a69b-4282-81e4-36306c2a8971)


## **Exploratory Data Analysis**
Before diving into the modeling process, the cleaned data is explored through visualizations and statistical summaries. This step allows us to understand the distribution of sentiments in the dataset, identify any patterns or trends, and gain valuable insights that may influence the modeling approach.
![positive](https://github.com/AutomationKay/Data-Science-/assets/112325655/30b1e3d0-4c30-4321-a4ee-d68614e45fe6)
![bar frequent positive](https://github.com/AutomationKay/Data-Science-/assets/112325655/cc968a00-bf83-4e61-a0c2-d070e803f709)


![neutral](https://github.com/AutomationKay/Data-Science-/assets/112325655/dac187d5-4936-47cd-a557-4a2565c04b54)
![bar frequent neutral](https://github.com/AutomationKay/Data-Science-/assets/112325655/539c96af-a8bd-405b-acce-801eda3f979a)


![negative](https://github.com/AutomationKay/Data-Science-/assets/112325655/841f6f90-789f-4961-82b7-75dbaa94ca79)
![bar frequent negative](https://github.com/AutomationKay/Data-Science-/assets/112325655/094d114f-d64e-41ff-b6f8-6d69ae34f114)



## **Vectorization and Feature Engineering**
To build predictive models, the text reviews are converted into numerical representations. This process, known as vectorization, includes techniques like Count Vector and TF-IDF (Term Frequency-Inverse Document Frequency). The sentiment labels are encoded to numeric values for classification.


## **Model Selection and Training**
Multiple machine learning models are explored in this analysis, including Naive Bayes, Logistic Regression, and Support Vector Machines (SVM). Each model is trained on the training set and evaluated using the validation set. Performance metrics like accuracy, precision, recall, and F1 score are used to assess the models' effectiveness.

### Count Vector Summary
![Count-Vector Summary](https://github.com/AutomationKay/Data-Science-/assets/112325655/fd5c7b3b-1039-4503-aa61-453d783ea9f0)


### TFID Summary
![TFID summary](https://github.com/AutomationKay/Data-Science-/assets/112325655/1d38240d-248d-4b1f-83ee-31933400b37e)




## **Results**
The trained models are then tested on a separate test set to assess their performance on unseen data. The confusion matrix is used to visualize the performance of the models, providing a detailed breakdown of correct and incorrect predictions for each sentiment class.

The final analysis offers insights into the sentiment trends of customers and identifies the most effective models for sentiment prediction in the context of the given product reviews on Amazon.

Please refer to the notebook files for detailed code and step-by-step implementation of the analysis.

Feel free to explore the repository; any feedback or contributions are greatly appreciated!
