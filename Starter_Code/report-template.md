# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

# Purpose of Analysis 

The purpose of this analysis was to develop a predictive model to identify high-risk loans. By accurately predicting which loans are likely to default, lenders can make more informed decisions, manage risk better, and potentially reduce financial losses. This analysis aimed to build a logistic regression model to classify loans as either healthy (0) or high-risk (1).

* Explain what financial information the data was on, and what you needed to predict.

# The dataset contained various financial features related to individual loans, including:

    -loan_size: The size of the loan.
    -interest_rate: The interest rate of the loan.
    -borrower_income: The income of the borrower.
    -debt_to_income: The debt-to-income ratio of the borrower.
    -num_of_accounts: The number of accounts the borrower has.
    -derogatory_marks: The number of derogatory marks on the borrower's credit report.
    -total_debt: The total debt of the borrower.
    -loan_status: The target variable indicating whether the loan is healthy (0) or high-risk (1).

# Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    The target variable, loan_status, was a binary variable

# Describe the stages of the machine learning process you went through as part of this analysis.
    
    1) Data Preparation: Loaded the dataset, examined its structure, and separated the features (X) from the target variable (y).

    2) Data Splitting: Split the data into training and testing sets to evaluate the model's performance on unseen data.

    3) Model Selection and Training: Chose the logistic regression algorithm for its simplicity and     interpretability, and trained the model on the training data.

    4) Making Predictions: Used the trained model to make predictions on the testing data.

    5) Evaluation: Evaluated the model's performance using a confusion matrix and classification report to assess precision, recall, and F1 score for both classes.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

    Logistic Regression: This algorithm was chosen for its effectiveness in binary classification problems and its ability to provide probabilistic outputs.

    
    Confusion Matrix and Classification Report: These evaluation tools provided detailed insights into the model's performance across both classes (healthy and high-risk loans).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

The logistic regression model was evaluated based on its ability to predict loan statuses as either healthy (0) or high-risk (1). The performance metrics used included accuracy, precision, recall, and F1 score, derived from the confusion matrix and classification report.

* Which one seems to perform best? How do you know it performs best?
The logistic regression model performs well, achieving high accuracy and strong performance metrics for both healthy and high-risk loans. Based on the evaluation metrics, it is clear that the logistic regression model is effective for this classification task.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Class 0 (Healthy Loans): Since healthy loans are the majority class, having high accuracy and precision for this class helps maintain low false positives, which means fewer loans are incorrectly flagged as high-risk.

Class 1 (High-Risk Loans): Predicting high-risk loans accurately is crucial for minimizing financial risk. High recall for this class (0.91) ensures that most high-risk loans are identified, reducing the likelihood of unexpected defaults.

If you do not recommend any of the models, please justify your reasoning.

Business Objective: If the primary goal is to minimize financial risk by identifying as many high-risk loans as possible, recall for class 1 becomes particularly important.

Logistic Regression: Given the high recall (0.91) for class 1, the logistic regression model is recommended. It strikes a good balance between precision and recall, ensuring that most high-risk loans are identified without an excessive number of false positives.

## Final Recommendation:
Use the Logistic Regression Model: The model performs well across all key metrics and is particularly effective at identifying high-risk loans, which is essential for managing financial risk. Its high accuracy and balanced performance make it a reliable choice for predicting loan statuses in this dataset.

By using this model, lenders can better manage their portfolios, make more informed lending decisions, and reduce the likelihood of financial losses due to defaults.
