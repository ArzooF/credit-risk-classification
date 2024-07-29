# Module 12 Report Template

## Overview of the Analysis
The purpose of this analysis is to evaluate the performance of a logistic regression model in predicting loan statuses using financial data. The goal is to determine whether the model can reliably distinguish between healthy loans (class 0) and high-risk loans (class 1) to assist the company in making informed lending decisions.

## Results
The dataset contains financial information on various loans, including details such as loan amount, interest rate, borrower income, debt-to-income ratio, and other relevant metrics. The primary objective is to predict the loan status, identifying whether a loan is healthy (class 0) or high-risk (class 1).

### Variables of Interest
The main variable we aim to predict is the loan_status, which has two classes:

Healthy Loan (0): Loans that are expected to be repaid without issues.
High-Risk Loan (1): Loans that are likely to default or face repayment challenges.
value_counts for loan_status shows that there are 75,036 healthy loans and 2,500 high-risk loans, indicating a significant class imbalance.

### Stages of the Machine Learning Process
1. Data Collection and Preparation:

Collected and loaded the lending_data.csv file into a Pandas DataFrame.
Separated the features (X) from the labels (y).

2. Data Splitting:

Split the dataset into training and testing sets using train_test_split to ensure the model is evaluated on unseen data.

3. Model Selection and Training:

Chose the LogisticRegression algorithm for its simplicity and effectiveness in binary classification tasks.
Trained the logistic regression model using the training data (X_train and y_train).

4. Model Evaluation:

Made predictions on the testing data (X_test).
Evaluated the model's performance using a confusion matrix and classification report, which provided precision, recall, and F1-scores for both classes.

5. Results Interpretation and Recommendation:

Analyzed the performance metrics to determine the model's effectiveness in predicting both healthy and high-risk loans.
Provided a recommendation based on the evaluation results.

### Methods Used
-- Logistic Regression:
1. Selected for its robustness in binary classification tasks.
2. Implemented using the LogisticRegression class from sklearn.linear_model.
3. Configured with a random_state parameter to ensure reproducibility.
4. Evaluated using metrics such as accuracy, precision, recall, and F1-score, which are crucial for understanding the model's performance.

### Model Performance Metrics
- Accuracy: 0.99
- Precision:
Healthy Loans (class 0): 1.00
High-Risk Loans (class 1): 0.87
- Recall:
Healthy Loans (class 0): 1.00
High-Risk Loans (class 1): 0.89


## Summary

The logistic regression model has demonstrated excellent performance in predicting loan statuses:

- High Accuracy: With an overall accuracy of 99%, the model makes very few errors, indicating it is highly effective at predicting loan outcomes.
- Perfect Precision and Recall for Healthy Loans: The model achieves perfect scores (1.00) for both precision and recall when predicting healthy loans. This means it correctly identifies all healthy loans without any false positives or false negatives.
- Strong Performance for High-Risk Loans: Although slightly lower than for healthy loans, the model still performs well in predicting high-risk loans, with a precision of 0.87 and recall of 0.89. This indicates the model correctly identifies most high-risk loans, with a relatively low rate of false positives and false negatives.

### Justification for Recommendation
Based on the evaluation results, I recommend the logistic regression model for use by the company. The model's high accuracy and near-perfect performance in predicting healthy loans, combined with its strong performance in identifying high-risk loans, make it a reliable tool for lending decisions. Implementing this model can help the company minimize the risk of defaults by accurately identifying high-risk loans while efficiently approving healthy loans. This balance ensures that the company can manage risk effectively while maintaining a high approval rate for low-risk loans.







