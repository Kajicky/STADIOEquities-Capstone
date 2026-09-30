# Data Preprocessing

## Purpose

The purpose of data preprocessing is to prepare the public Credit Card Customers dataset for machine learning by cleaning the data, removing irrelevant variables, transforming categorical variables, and preparing the target variable for modelling.

## Dataset

The dataset used is the **Credit Card Customers (BankChurners)** dataset identified in Part A.

The target variable is:

* `Attrition_Flag`

The target contains two classes:

* Existing Customer
* Attrited Customer

## Preprocessing Techniques

The following preprocessing techniques will be applied:

### 1. Remove irrelevant columns

The following columns will be removed because they do not provide useful predictive information:

* `CLIENTNUM` – customer identification number.
* `Naive_Bayes_Classifier_Attrition_Flag_Card_Category_Contacts_Count_12_mon`
* `Naive_Bayes_Classifier_Attrition_Flag_Income_Category_Gender`

The two Naive Bayes columns are removed because they contain outputs from another predictive model rather than original customer information.

### 2. Separate features and target

The target variable, `Attrition_Flag`, will be separated from the predictor variables.

The remaining variables will be used as input features for the machine learning models.

### 3. Encode categorical variables

Categorical variables will be converted into numerical representations so that they can be used by machine learning algorithms.

One-hot encoding will be used where appropriate.

### 4. Encode the target variable

The target variable will be converted into a binary numerical format:

* Existing Customer → 0
* Attrited Customer → 1

### 5. Train-test split

The dataset will be divided into training and testing datasets.

A stratified split will be used to preserve the proportion of the two customer classes in both datasets.

### 6. Feature scaling

Numerical features will be scaled where required.

Scaling is particularly relevant for the Logistic Regression model because variables measured on different scales can affect the model's coefficients.

### 7. Class imbalance

The distribution of the target classes will be examined because the dataset contains substantially more existing customers than attrited customers.

The training data will be considered for class-balancing techniques where necessary.

## Related Code

The preprocessing implementation will be provided in:

`preprocessing.ipynb`

The notebook will contain the actual Python code used to perform the preprocessing steps described above.

## How to Use

The preprocessing notebook should be run from beginning to end after the BankChurners dataset has been placed in the project directory.

The resulting processed dataset will then be used by the feature engineering and modelling stages.
