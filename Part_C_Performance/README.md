# Part C – Model Performance

## Overview

This section presents the results obtained from applying the two machine-learning models developed in Part B to the Credit Card Customers (BankChurners) public dataset.

The models evaluated were:

1. **Model 1 – Logistic Regression**
2. **Model 2 – XGBoost**

Both models were evaluated using the same 80/20 stratified train-test split with `random_state = 42`.

## Performance Documentation

* [Model 1 Performance – Logistic Regression](Model1Performance.MD)
* [Model 2 Performance – XGBoost](Model2Performance.MD)
* [Model Comparison](Comparison.MD)

## Supporting Notebook

The complete modelling and performance evaluation workflow is available in:

* [Part C Performance Notebook](part_c_performance.ipynb)

The notebook includes:

1. Loading the BankChurners dataset.
2. Data preprocessing.
3. Feature engineering.
4. One-hot encoding.
5. Stratified train-test splitting.
6. Logistic Regression training and evaluation.
7. XGBoost training and evaluation.
8. Calculation of Accuracy, Precision, Recall, F1-score and ROC-AUC.
9. Comparison of the two models.

## Key Results

| Metric    | Logistic Regression | XGBoost |
| --------- | ------------------: | ------: |
| Accuracy  |              0.8657 |  0.9630 |
| Precision |              0.5538 |  0.8592 |
| Recall    |              0.8400 |  0.9200 |
| F1-score  |              0.6675 |  0.8886 |
| ROC-AUC   |              0.9421 |  0.9924 |

The results represent performance on the held-out test set of the public BankChurners dataset. Further validation would be requir
