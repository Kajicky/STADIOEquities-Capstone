# Publication 2 – Peng, Peng and Li (2023)

## Title

Research on customer churn prediction and model interpretability analysis

## Harvard Reference

Peng, K., Peng, Y. and Li, W. (2023) ‘Research on customer churn prediction and model interpretability analysis’, *PLOS ONE*, 18(12), e0289724.

## Link

https://doi.org/10.1371/journal.pone.0289724

## Modelling

The study compared six machine-learning classification models: XGBoost, LightGBM, Decision Tree, K-Nearest Neighbours (KNN), Gradient Boosting Decision Tree (GBDT), and Extra Trees. XGBoost was subsequently optimised using a Genetic Algorithm (GA), producing a GA-XGBoost model. SHAP was also used to interpret the model's predictions.

## Preprocessing Techniques

The researchers performed data cleaning and transformation, removed a highly correlated feature (Avg_Utilization_Ratio), converted categorical variables using one-hot encoding, and applied Z-score normalisation. They also investigated class imbalance using oversampling and hybrid resampling approaches, including SMOTE, ADASYN and SMOTEENN.

## Dataset Used

The study used the Credit Card Customer dataset (BankChurners) obtained from Kaggle. The dataset contains demographic, behavioural and transaction information about bank customers and includes an attrition indicator.

## Key Takeaways

1. Class imbalance can substantially affect customer-churn prediction, making techniques such as SMOTEENN useful to investigate.
2. XGBoost can provide strong predictive performance for customer-churn classification, particularly when combined with hyperparameter optimisation.
3. SHAP can make complex models more interpretable by showing which customer characteristics contribute to churn predictions.

## Relevance to STADIOEquities

This study is relevant because it uses customer demographic, behavioural and transaction information to predict attrition. These are the types of variables that could potentially be useful when predicting customer dormancy. The use of SHAP is also relevant because STADIOEquities would benefit from understanding which factors contribute to the prediction.
