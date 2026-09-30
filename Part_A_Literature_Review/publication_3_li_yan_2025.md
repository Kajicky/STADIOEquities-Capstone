# Publication 3 – Li and Yan (2025)

## Title

Prediction of bank credit customers churn based on machine learning and interpretability analysis

## Harvard Reference

Li, Y. and Yan, K. (2025) ‘Prediction of bank credit customers churn based on machine learning and interpretability analysis’, *Data Science in Finance and Economics*, 5(1), pp. 19–34.

## Link

https://doi.org/10.3934/DSFE.2025002

## Modelling

The study evaluated six machine-learning methods: Random Forest (RF), Gradient Boosting Decision Tree (GBDT), Extra Trees, AdaBoost, XGBoost and CatBoost. Four sampling approaches were investigated: Random Oversampling, SMOTE, Borderline-SMOTE and ADASYN. SHAP was used for model interpretation, while an R-learner was used for causal analysis.

## Preprocessing Techniques

The researchers removed the customer identifier and irrelevant Naive Bayes output columns, converted categorical variables into numerical representations, replaced “Unknown” categories with the majority class for selected categorical variables, normalised independent variables, and divided the dataset into an 80% training and 20% test set. The training data was balanced using four sampling techniques.

## Dataset Used

The study used a bank customer churn dataset downloaded from Kaggle, containing 10,127 customer records. The dataset includes demographic information, credit-card characteristics and customer transaction and behavioural information.

## Key Takeaways

1. Class imbalance is an important consideration in customer-churn modelling, and different resampling techniques can be compared before selecting an approach.
2. XGBoost performed strongly across the different sampling approaches used in the study.
3. SHAP can be used to identify important behavioural variables, including transaction counts, transaction amounts and the number of products held by customers.

## Relevance to STADIOEquities

This study is relevant because it demonstrates how demographic, financial and behavioural information can be used to predict customer attrition. Transaction activity and the number of products held by a customer can provide useful information when developing a customer-dormancy model.
