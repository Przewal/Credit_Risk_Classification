# Credit Risk Analysis

## Overview of the Analysis

The purpose of this analysis was to assess the performance of logistic regression models in predicting credit risk using financial data. The task involved predicting whether a loan is healthy (0) or has a high risk of defaulting (1) based on various features in the dataset. Two models were trained and evaluated: one using the original data and another using resampled data to address class imbalance.

## Results

### Machine Learning Model 1: Logistic Regression with Original Data

- Balanced Accuracy Score: __99.18%__
- Precision and Recall Scores:
  - Class 0 (Healthy Loan):
    - Precision: __100%__
    - Recall: __99%__
    - F1-Score: __100%__
  - Class 1 (High-Risk Loan):
    - Precision: __85%__
    - Recall: __91%__
    - F1-Score: __88%__

### Machine Learning Model 2: Logistic Regression with Resampled Data

- Balanced Accuracy Score: __99.38%__
- Precision and Recall Scores:
  - Class 0 (Healthy Loan):
    - Precision: __100%__
    - Recall: __99%__
    - F1-Score: __100%__
  - Class 1 (High-Risk Loan):
    - Precision: __84%__
    - Recall: __99%__
    - F1-Score: __91%__

## Summary

The logistic model using the original data indicates an accuracy of 99%, the precision score is almost 100% for class 0 i.e., for a healthy loan but lower for the cases where the loan can default. Same follows for recall (sensitivity) and f1-score. A high accuracy does not necessarily indicate that the model works well, rather it suggests that there is a greater probability of overfitting as the accuracy vs precision/recall do not match well. Due to the class imbalance, it struggled in correctly predicting the high-risk loans (Class 1), with a low recall score indicating a high number of false negatives.

After employing RandomOverSampler to address the imbalance, the model trained on resampled data demonstrated improvement in predicting high-risk loans, as evidenced by increased recall for Class 1. The balanced accuracy score also showed enhancement compared to the original model.

### Recommendation

Considering the task of predicting high-risk loans is crucial in financial risk assessment, the model trained on resampled data outperforms the original data model in identifying these cases. Hence, the recommendation is to use the logistic regression model trained with the resampled data for credit risk prediction, as it provides better recall and balanced accuracy for identifying high-risk loans.
