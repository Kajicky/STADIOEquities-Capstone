# Model 2 Performance – XGBoost

## 1. Overview

XGBoost was used as Model 2 to predict customer attrition in the Credit Card Customers (BankChurners) dataset.

The model was trained using an 80/20 stratified train-test split with `random_state = 42`.

The model configuration was:

- `n_estimators = 200`
- `max_depth = 4`
- `learning_rate = 0.05`
- `subsample = 0.8`
- `colsample_bytree = 0.8`
- `scale_pos_weight = 5.22`
- `random_state = 42`
- `eval_metric = logloss`

The target variable was encoded as:

- Existing Customer = 0
- Attrited Customer = 1

Categorical variables were one-hot encoded before training.

## 2. Class Imbalance

The training data contained:

- Existing Customers: **6,799**
- Attrited Customers: **1,302**

The class imbalance ratio was used to calculate `scale_pos_weight`:

**5.22**

This parameter was used to give greater consideration to the minority attrited-customer class during model training.

## 3. Performance Metrics

The XGBoost model was evaluated using Accuracy, Precision, Recall, F1-score and ROC-AUC.

| Metric | Result |
|---|---:|
| Accuracy | 0.9630 |
| Precision | 0.8592 |
| Recall | 0.9200 |
| F1-score | 0.8886 |
| ROC-AUC | 0.9924 |

## 4. Interpretation of Results

The XGBoost model achieved an accuracy of **96.30%**.

The precision of **85.92%** indicates that, among customers predicted as attrited, 85.92% were actually attrited customers.

The recall of **92.00%** indicates that the model identified 92.00% of the customers who were actually classified as attrited.

The F1-score of **0.8886** provides a combined measure of precision and recall.

The ROC-AUC of **0.9924** indicates strong discrimination between existing and attrited customers across different classification thresholds.

Because the dataset contains an imbalanced target variable, recall, F1-score and ROC-AUC were considered alongside accuracy.

## 5. Statistical Method

The model was evaluated using a held-out test set containing 20% of the observations. A stratified split was used to maintain the class distribution between the training and testing datasets.

The evaluation metrics were calculated from the test-set predictions.

## 6. Related Code

The Model 2 performance calculations are contained in:

`part_c_performance.ipynb`

The notebook includes:

1. Loading the BankChurners dataset.
2. Data preparation and feature engineering.
3. One-hot encoding.
4. Stratified train-test splitting.
5. Calculation of class imbalance.
6. XGBoost training.
7. Prediction generation.
8. Calculation of performance metrics.

## 7. How to Use

Open `part_c_performance.ipynb` in Google Colab.

Upload `BankChurners.csv` to the Colab environment and run the notebook cells from beginning to end.

The notebook will reproduce the XGBoost performance metrics reported above.
