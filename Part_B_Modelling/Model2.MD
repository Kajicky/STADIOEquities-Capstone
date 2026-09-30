# Model 2 – XGBoost

## Purpose

XGBoost will be used as the second machine learning model for predicting customer attrition.

XGBoost is a gradient-boosting algorithm that can model complex relationships between customer characteristics and attrition outcomes.

It was selected because XGBoost was also investigated in the literature reviewed in Part A.

## Model Technique

The model used is **Extreme Gradient Boosting (XGBoost)**.

The target variable is:

* `Attrition_Flag`

The target is represented as:

* Existing Customer → 0
* Attrited Customer → 1

## Model Configuration

The following hyperparameter values will be used:

* `n_estimators = 200` – number of boosting trees.
* `max_depth = 4` – maximum depth of each tree.
* `learning_rate = 0.05` – controls the contribution of each tree.
* `subsample = 0.8` – proportion of training observations used for each tree.
* `colsample_bytree = 0.8` – proportion of features used for each tree.
* `random_state = 42` – ensures reproducibility.

The model will therefore be configured using these fixed values to provide a reproducible baseline for comparison with Logistic Regression.

## Input Data

The model will use the feature-engineered dataset.

The dataset contains:

* Customer demographic information
* Account and relationship information
* Transaction behaviour
* Customer inactivity
* Engineered transaction features

Categorical variables will be converted into numerical variables using one-hot encoding.

## Class Imbalance

The dataset contains more Existing Customers than Attrited Customers.

The XGBoost model will account for this imbalance using the `scale_pos_weight` parameter. The value will be calculated from the training data as:

`number of negative-class observations / number of positive-class observations`

This allows the model to give greater consideration to the minority Attrited Customer class.

## Model Training

The dataset will be divided into training and testing sets using a stratified 80/20 split.

The model will be trained using the training data and evaluated using the testing data.

## Evaluation Metrics

The following metrics will be used:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion matrix

The results will allow the performance of XGBoost to be compared with the Logistic Regression baseline.

## Related Cod
