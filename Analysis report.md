# Module 12 Credit-Risk-Classification Challenge 

# Loan Prediciton Analysis 

## Overview
This project involves building a predictive model to classify loans as either healthy or high-risk. The objective is to assist financial institutions in evaluating loan applications more effectively by predicting the risk associated with each loan. 

## Purpose
The purpose of this anaylsis is to develop a model that accurately classifies loans into two categories based on financial attributes: 
- **Healthy Loan** (label `0`)
- **High-Risk Loan** (label `1`)

## Data
The dataset contains various financial attributed related to loan applications, including:
- Loan size, Interest rate, Interest rate, Borrower income, Debt relation to income, Number of accounts, Deragatory marks, Total debt, and loan status. 
The target variable to predict is the loan status, with the following classes:
- `0` (Healthy Loan)
- `1` (High-Risk Loan)

## Machine Learning Process
1. Data preparation
- Load the Dataset: Import and read csv file (lending_data.csv).
- Feature and Label Extraction: Extract the target labels(`y`) from the "loan status" column and define the feature matrix (`X) by excluding the target column. 
- Train-Test Split: Split the data into training and testing sets using `train_test_split`. 

2. Model Building and Evaluation
- Model Intialization: Intialize a lLogistic regression Model.
- Model training: Fit the Logistic Regression model on the training data (X_train and Y_train)
- Model Prediciton: Generate predictions on the testing dataset using the trained mode. 

3. Model Evaluation
- Confusion Matrix: Compute the confusion matrix to evaluate the model's performance. 
- Classification Report: Generate and print the classification report to assess precision, recall, and F1-score. 

## Model performance Summary
### Model Evaluation
- **Accuracy Score:** 0.9918
- Indicates that the model correctly predicted the loan status 99.18% of the time across all classes. 

- **Precision:** 
    - **Healthy Loans:** 1.00
        - The model made perfect prediction for healthy loans, which means all predicted healthy loans were actually healthy. 
    - **High-Risk Loans:** 0.85
        - The precision for high risk loans is 85%, meaning 85% pf the predicted high risk loans were certainly high risk, with 15% being false positive. 

- **Recall:** 
    - **Healthy Loans:** 0.99
        - The model successfully identified 99% of the actual healthy loans. 
    - **High-Risk Loans:** 0.91
        - The recall for high-risk loans is 91%, indicating model correctly identified 91% of the actual high-risk loans, with 9% being false negatives. 

- **Reccomendation:** Given the high overall accuracy and balanced metrics, the logistic regression model is effective for predicting both healthy and high-risk loans, but it could be potentially be improved for high-risk loans to reduce the number of false negatives. 