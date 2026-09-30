# Model Comparison – Logistic Regression vs XGBoost

## 1. Overview

Two machine-learning models were evaluated for predicting customer attrition using the Credit Card Customers (BankChurners) public dataset:

- **Model 1:** Logistic Regression
- **Model 2:** XGBoost

Both models used the same dataset, feature engineering process and stratified 80/20 train-test split with `random_state = 42`.

## 2. Performance Comparison

| Metric | Logistic Regression | XGBoost |
|---|---:|---:|
| Accuracy | 0.8657 | 0.9630 |
| Precision | 0.5538 | 0.8592 |
| Recall | 0.8400 | 0.9200 |
| F1-score | 0.6675 | 0.8886 |
| ROC-AUC | 0.9421 | 0.9924 |

## 3. Accuracy

Logistic Regression achieved an accuracy of **86.57%**, while XGBoost achieved **96.30%** on the test dataset.

Accuracy represents the proportion of all test observations that were classified correctly.

Because the dataset contains an imbalanced target variable, accuracy was considered together with precision, recall, F1-score and ROC-AUC.

## 4. Precision

Logistic Regression achieved a precision of **55.38%**, compared with **85.92%** for XGBoost.

Precision measures the proportion of customers predicted as attrited who were actually attrited.

## 5. Recall

Logistic Regression achieved a recall of **84.00%**, while XGBoost achieved **92.00%**.

Recall measures the proportion of actual attrited customers that were correctly identified by the model.

Recall is particularly relevant to a customer-dormancy or attrition problem because failing to identify an attrited or at-risk customer may reduce the opportunity for a retention intervention.

## 6. F1-score

The Logistic Regression model achieved an F1-score of **0.6675**, while XGBoost achieved **0.8886**.

The F1-score combines precision and recall into a single measure and is useful when the classes are imbalanced.

## 7. ROC-AUC

Logistic Regression achieved a ROC-AUC of **0.9421**, while XGBoost achieved **0.9924**.

ROC-AUC measures the model's ability to distinguish between the two classes across different classification thresholds.

## 8. Statistical Evaluation Approach

Both models were evaluated using the same held-out test dataset.

The dataset was divided using an **80/20 stratified train-test split**, ensuring that the relative proportions of existing and attrited customers were maintained between the training and testing sets.

The following performance measures were calculated from the test-set predictions:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

The comparison therefore uses the same evaluation dataset and metrics for both models.

## 9. Summary

The results show measurable differences between the two modelling approaches across all five reported evaluation metrics.

| Metric | Difference (XGBoost − Logistic Regression) |
|---|---:|
| Accuracy | +0.0973 |
| Precision | +0.3054 |
| Recall | +0.0800 |
| F1-score | +0.2211 |
| ROC-AUC | +0.0503 |

These results demonstrate that the two models produce different levels of predictive performance on the public dataset. The results provide evidence that model selection can materially affect the identification of customer attrition.

Further validation would be required before applying the modelling approach to STADIOEquities' sensitive customer data.

## 10. Related Code

The performance comparison was produced using:

`part_c_performance.ipynb`

The notebook contains the complete workflow for:

1. Loading the public dataset.
2. Preparing the data.
3. Creating engineered features.
4. Splitting the dataset.
5. Training Logistic Regression.
6. Training XGBoost.
7. Generating predictions.
8. Calculating the evaluation metrics.
9. Producing the model comparison table.

## 11. How to Use

Open `part_c_performance.ipynb` in Google Colab.

Upload `BankChurners.csv` and run the notebook from beginning to end.

The notebook will reproduce the performance metrics and comparison reported in this document.
