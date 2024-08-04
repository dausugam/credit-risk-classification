# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The purpose of fitting a logistic regression model to identify the creditworthiness of borrowers is to create a predictive tool that can determine the likelihood of a borrower defaulting on a loan. It aims to improve risk management, enhance decision-making, and streamline the credit evaluation process, ultimately contributing to the financial stability and efficiency of lending institutions.

* Explain what financial information the data was on, and what you needed to predict.

To predict if there is high risk in the loan, we have the following variables: loan size, interest rate, borrower income, debt to income, number or accounts, derogatory marks and total debt.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The value we are trying to predict is the `loan_status`, where a value of 0 means that the loan is healthy and a value of 1 means that the loan has a high risk of defaulting.

* Describe the stages of the machine learning process you went through as part of this analysis.

    * Split the Data into Training and Testing Sets
    * Fit a logistic regression model by using the training data
    * Create prediction with the model using the Test Data (X values)
    * Evaluate the model’s performance by comparing the predictions with the `y` values of the test data

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithm).

Logistic regression is a statistical method for predicting binary outcomes from data. Each data point receives a probability of being in the `1` category, if the probability is abvove certain threshold, that data point is estimated to be a `1`, below that threshold, the data point is a `0`.

Logistic regression converts using a Sigmoind (or Squashing) function.

Overall, logistic regression is a simple yet powerful tool for classification tasks, especially when the relationship between the input features and the output is approximately linear.

## Results

Describe the accuracy scores and the precision and recall scores of the machine learning model.

* Healthy Loan
    * Precision: 0.99
    This means that 99% of the instances predicted as "Healthy Loan" were indeed healthy loans. There are very few false positives, indicating that the model is highly accurate when it predicts a loan to be healthy.
    * Recall: 1.00
    This means that the model correctly identified 100% of actual healthy loans. There are no false negatives, which indicates that the model captures all healthy loans without missing any.

* High Risk
    * Precision: 0.94
    This means that 94% of the instances predicted as "High Risk" were indeed high-risk loans. The model has a good precision, though there are some false positives.
    * Recall: 0.84
    This means that the model correctly identified 84% of the actual high-risk loans. The recall is slightly lower, indicating that the model misses some high-risk loans (false negatives).

* Overall Metrics
    * Accuracy: 0.99
    The overall accuracy of the model is 99%, meaning that the vast majority of predictions (both healthy and high-risk) are correct. This high accuracy suggests that the model performs very well on the given dataset.

## Summary

The logistic regression model demonstrates excellent performance in predicting the creditworthiness of borrowers. The model has particularly high precision and recall for healthy loans, ensuring that almost all healthy loans are correctly identified with minimal false positives. While the model is slightly less accurate for high-risk loans, it still maintains a good balance of precision and recall, capturing most high-risk loans correctly. The high overall accuracy indicates that the model is reliable and effective for practical use in assessing borrower creditworthiness.
