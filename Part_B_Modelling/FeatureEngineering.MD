# Feature Engineering

## Purpose

Feature engineering involves creating or transforming variables to provide the machine learning models with useful information about customer behaviour.

The objective is to identify features that may help explain customer attrition and engagement.

## Engineered Features

### 1. Average Transaction Amount

A new feature called `Avg_Transaction_Amount` will be created using:

`Total_Trans_Amt / Total_Trans_Ct`

This represents the average transaction amount per transaction and provides an additional measure of customer transaction behaviour.

### 2. Transaction Activity

The existing variables:

* `Total_Trans_Amt`
* `Total_Trans_Ct`
* `Total_Ct_Chng_Q4_Q1`
* `Total_Amt_Chng_Q4_Q1`

will be retained because they provide information about customer transaction activity and changes in behaviour.

### 3. Customer Inactivity

The existing `Months_Inactive_12_mon` variable will be retained as an important behavioural feature.

Higher inactivity may indicate reduced customer engagement and may therefore be relevant to predicting attrition.

### 4. Customer Relationship

The existing `Total_Relationship_Count` variable will be retained to represent the number of products or services held by each customer.

This provides information about the customer's relationship with the financial institution.

## Feature Selection

The engineered and existing features will be reviewed before modelling.

Features that do not provide useful predictive information, such as customer identification numbers, will not be used.

Feature engineering will be performed using the training data workflow to avoid introducing information from the test dataset into the modelling process.

## Related Code

The feature engineering implementation will be provided in:

`feature_engineering.ipynb`

The notebook will contain the Python code used to create the engineered features.

## How to Use

The notebook should be run after the preprocessing stage.

The resulting dataset will then be used as input for the machine learning models.
