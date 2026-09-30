# Model 1 Performance – Logistic Regression

## 1. Overview

Logistic Regression was used as Model 1 to predict customer attrition in the Credit Card Customers (BankChurners) dataset.

The model was trained using an 80/20 stratified train-test split with `random_state = 42`.

The model configuration was:

* `max_iter = 1000`
* `class_weight = "balanced"`
* `random_state = 42`

The target variable was encoded as:

* Existing Customer = 0
* Attrited Customer = 1

Categorical variables were one-hot encoded and numerical variables were standardised before training.

## 2. Performance Metrics

The model was evaluated using Accuracy, Precision, Recall, F1-score and ROC-AUC.

| Metric    | Result |
| --------- | -----: |
| Accuracy  | 0.8657 |
| Precision | 0.5538 |
| Recall    | 0.8400 |
| F1-score  | 0.6675 |
| ROC-AUC   | 0.9421 |

## 3. Interpretation of Results

The Logistic Regression model achieved an accuracy of **86.57%**.

The precision of **55.38%** indicates that, among customers predicted as attrited, 55.38% were actually attrited customers.

The recall of **84.00%** indicates that the model identified 84.00% of the customers who were actually classified as attrited.

The F1-score of **0.6675** provides a combined measure of precision and recall.

The ROC-AUC of **0.9421** indicates strong discrimination between existing and attrited customers across different classification thresholds.

Because customer attrition is an imbalanced classification problem, recall, F1-score and ROC-AUC were considered alongside accuracy rather than relying on accuracy alone.

## 4. Statistical Evaluation Method

The model was evaluated on a held-out test set containing 20% of the observations. Stratification was used during the train-test split to maintain the class distribution between the training and testing datasets.

The evaluation metrics were calculated from the test-set predictions.

## 5. Related Code

The Model 1 performance calculations are contained in:

`part_c_performance.ipynb`

The notebook includes:

1. Loading the BankChurners dataset.
2. Data preparation and feature engineering.
3. One-hot encoding.
4. Stratified train-test splitting.
5. Logistic Regression training.
6. Prediction generation.
7. Calculation of performance metrics.

## 6. How to Use

Open `part_c_performance.ipynb` in Google Colab.

Upload `BankChurners.csv` to the Colab environment and run the notebook cells from beginning to end.

The notebook will reproduce the Logistic Regression performance metrics reported above.

