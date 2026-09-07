# STADIOEquities-Capstone
Capstone project on client dormancy
# STADIOEquities Capstone Project

## 1. Project Motivation

### Reducing Client Dormancy and Improving Client Engagement at STADIOEquities

---

STADIOEquities operates in the South African retail investment and fintech industry, where digital platforms have made investing more accessible to ordinary people. The company has grown to approximately 2.3 million registered accounts, showing that there is strong interest in digital investing. However, not all of these registered clients become active investors. According to the briefing pack, only about 760,000 accounts are funded and active, while 41% of registered accounts have never been funded. This suggests that although STADIOEquities is successful in attracting clients, keeping them active and engaged remains a challenge.

This project is motivated by the need to better understand why some clients remain active while others stop using the platform or become dormant. In particular, the study will focus on client dormancy and the factors that may be associated with a client becoming inactive within six months. STADIOEquities has several years of historical information that could help provide insight into this issue. This includes information about account registration and funding, trading activity, client demographics, app and website behaviour, and marketing engagement. For the project to be successful, the relevant historical data needs to be sufficiently complete, reliable and possible to link at client level.

The issue is important because STADIOEquities is already experiencing changes in its customer engagement indicators. The conversion rate from sign-up to first deposit has decreased from 64% to 59%, while the percentage of accounts becoming dormant within six months has increased from 22% to 31%. These changes are concerning because the company spends approximately R180 to acquire an account, but an account that remains empty or inactive provides limited value to the business. Since STADIOEquities generates revenue through activities such as assets under administration, trading, cash balances and subscriptions, clients who remain engaged are important to the long-term sustainability of the platform.

Another reason for conducting this study is that STADIOEquities currently deals with a very diverse group of clients. Some clients may save and invest every month, while others may make occasional trades, invest in a single stock, or register an account without ever making a deposit. Despite these differences, the briefing pack indicates that many of the company's communications, nudges and product suggestions are delivered in a relatively standardized way. This creates an opportunity to use the information already available to better understand different client behaviours.

Data science could contribute to addressing this challenge by identifying patterns in historical client behaviour that may be linked to continued engagement or future dormancy. For example, analysing funding activity, trading behaviour, platform usage and other relevant characteristics could help identify clients who show signs of becoming inactive. This would not mean that data science can prevent every client from becoming dormant, but it could give STADIOEquities better information to support decisions about which clients may need additional engagement and when that engagement may be appropriate.

The study is also relevant to STADIOEquities' longer-term strategy, particularly its aim to activate existing accounts and keep clients engaged over time. Instead of relying mainly on broad assumptions about its customers, the company could use evidence from its historical data to understand its clients more effectively. This could help marketing, product and client-service teams make better-informed decisions and use their resources more efficiently.

Overall, the motivation for this project comes from a clear gap between the number of people who register with STADIOEquities and the number who become active and remain engaged investors. Understanding the factors associated with client dormancy could help the company make better use of the customer data it already collects, improve its approach to client engagement and support its goal of building a more active and sustainable client base.

---

## 2. Problem Statement

---

STADIOEquities has a large customer base of approximately **2.3 million** registered accounts, but a significant number of these clients do not become active investors or remain engaged with the platform. The sign-up-to-first-deposit conversion rate has declined from **64% to 59%**, while accounts becoming dormant within six months have increased from **22% to 31%**. This presents a challenge for STADIOEquities because the company invests in acquiring clients, while inactive and unfunded accounts generate limited value.

Despite having several years of historical client data, it remains unclear which client characteristics and behaviours are associated with clients becoming dormant. STADIOEquities has information on account and funding activity, trading behaviour, app and website usage, client demographics and marketing engagement, which could provide useful insight into patterns of client engagement.

Therefore, this study aims to investigate the factors associated with client dormancy and use the available historical data to develop a data-driven method for identifying clients who are more likely to become inactive. The findings could assist STADIOEquities in making more informed decisions about client activation and retention.
## Repository Structure

The following folder structure is used in this repository:

| Folder | Description |
|--------|-------------|
| `data/raw/` | Raw, unprocessed data received from STADIOEquities |
| `data/processed/` | Cleaned and preprocessed data ready for analysis |
| `notebooks/` | Jupyter notebooks for EDA, modeling, and evaluation |
| `models/` | Saved trained machine learning models |
| `scripts/` | Python scripts for preprocessing, training, evaluation, visualization, and statistical tests |
| `results/` | Experimental results, performance metrics, and charts |
| `results/charts/` | Visualizations and plots |
| `docs/` | Documentation, including the data request PDF |

### Key Files

| File | Description |
|------|-------------|
| `README.md` | Project overview, motivation, problem statement, and repository structure |
| `docs/Data_Request.pdf` | Detailed data request for the project |

### Experimental Setup

- **Environment:** Python 3.x
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn, xgboost
- **Models:** Logistic Regression, Random Forest, XGBoost
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-Score, AUC-ROC
- **Validation:** 5-fold cross-validation

### Scripts Overview

| Script | Purpose |
|--------|---------|
| `data_preprocessing.py` | Clean and prepare data |
| `statistical_tests.py` | Run statistical tests (t-test, chi-square, correlation) |
| `model_training.py` | Train machine learning models |
| `model_comparison.py` | Compare model performance |
| `group_comparison.py` | Compare client groups |
| `feature_analysis.py` | Analyze feature importance |
| `performance_metrics.py` | Calculate model evaluation metrics |
| `visualization.py` | Create charts and plots |

### Experimental Results

Results will be stored in the `results/` folder, including model performance metrics and visualizations in `results/charts/`.
## RAAIDD Log

---

### Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Data may have missing or incomplete values for key client features | Analysis may be inaccurate or incomplete | Perform data quality checks early; use imputation techniques or drop incomplete records |
| The dataset may be imbalanced (more active than dormant clients) | Model may perform poorly on dormant clients | Use techniques like SMOTE or class weighting to handle imbalance |
| Client data may not be easily linkable across different sources | Unable to create a unified client view | Request a consistent Client ID field across all datasets at the start |
| The model may not generalise well to future clients | Predictions may be unreliable | Use cross-validation and test on unseen data |
| Time constraints may limit the depth of analysis | May not explore all features or models | Prioritise key features and models; document limitations |

---

### Actions

| Action | Timeline | Status |
|--------|----------|--------|
| Obtain and review historical client data from STADIOEquities | Week 1 | Not Started |
| Perform exploratory data analysis (EDA) to understand client patterns | Week 1-2 | Not Started |
| Clean and preprocess data (handle missing values, outliers, encode categories) | Week 2 | Not Started |
| Split data into training and testing sets (80/20 split) | Week 2 | Not Started |
| Train baseline models (Logistic Regression, Random Forest) | Week 3 | Not Started |
| Train advanced models (XGBoost) | Week 3 | Not Started |
| Evaluate model performance using accuracy, precision, recall, F1, AUC-ROC | Week 3 | Not Started |
| Identify top features predicting client dormancy | Week 4 | Not Started |
| Create visualisations (ROC curves, confusion matrices, feature importance) | Week 4 | Not Started |
| Document findings and provide recommendations for STADIOEquities | Week 4 | Not Started |
| Update README.md with all project documentation | Ongoing | In Progress |

---

### Assumptions

| Assumption | Impact if False |
|------------|-----------------|
| The historical data provided is accurate and complete | Analysis and predictions may be unreliable |
| Client behaviour patterns from the past 6 years will continue to be relevant | Model may not predict future dormancy accurately |
| Client ID is consistent across all datasets (funding, trading, app usage) | Unable to link client data across sources |
| Dormancy is defined correctly as no activity within 6 months | Wrong clients may be labelled as dormant |
| The data provided is sufficient to build a predictive model | May need additional features not currently available |
| Clients who are active have similar characteristics to those who become dormant | Model may not learn patterns of dormancy effectively |

---

### Issues

| Issue | Date Identified | Impact | Resolution |
|-------|-----------------|--------|------------|
| No issues identified yet | - | - | Issues will be documented as they arise during the project |

---

### Decisions

| Decision | Rationale | Date Made |
|----------|-----------|-----------|
| Focus on dormancy within 6 months of registration | This is where the biggest increase (22% to 31%) was observed | Project Start |
| Use Python for analysis | Industry standard for data science projects | Project Start |
| Use 80/20 train-test split | Standard practice for model development | Project Start |
| Start with Logistic Regression as baseline | Simple, interpretable model to establish benchmark | Project Start |
| Use F1-Score as primary metric | Handles imbalanced data better than accuracy alone | Project Start |
| Limit analysis to clients who registered in the last 6 years | Available data history | Project Start |

---

### Dependencies

| Task | Depends On | Timeline |
|------|------------|----------|
| Data cleaning | Data being received from STADIOEquities | Week 2 |
| EDA | Data being cleaned | Week 2 |
| Model training | Data being split into train/test | Week 3 |
| Model evaluation | Model being trained | Week 3 |
| Feature importance analysis | Model being trained | Week 4 |
| Visualisations | Model evaluation being complete | Week 4 |
| Recommendations | All analysis being complete | Week 4 |
| Final README update | All tasks being complete | End of Project |

---

### Summary

| Category | Count |
|----------|-------|
| Risks Identified | 5 |
| Actions Planned | 11 |
| Assumptions Made | 6 |
| Issues Found | 0 (so far) |
| Decisions Made | 6 |
| Dependencies Identified | 8 |
## Repository Structure

The following folders are used in this repository:

| Folder | Description |
|--------|-------------|
| `Datasets/` | Raw and processed datasets used in the project |
| `Models/` | Saved trained machine learning models |
| `Experimental setup/` | Documentation of experimental configuration |
| `Experimental results/` | Experimental results, performance metrics, and charts |
| `Statistical helper and comparison scripts/` | Python scripts for statistical tests and model comparison |
| `Visualisation scripts/` | Python scripts for creating charts and plots |
| `notebooks/` | Jupyter notebooks for EDA, modeling, and evaluation |

### Key Files

| File | Description |
|------|-------------|
| `README.md` | Project overview, motivation, problem statement, and repository structure |
| `26305040_SS1_PartC_CAP182.pdf` | Detailed data request for the project (Part C) |
## RAAIDD Log

---

### Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Data may have missing or incomplete values for key client features | Analysis may be inaccurate or incomplete | Perform data quality checks early; use imputation techniques or drop incomplete records |
| The dataset may be imbalanced (more active than dormant clients) | Model may perform poorly on dormant clients | Use techniques like SMOTE or class weighting to handle imbalance |
| Client data may not be easily linkable across different sources | Unable to create a unified client view | Request a consistent Client ID field across all datasets at the start |
| The model may not generalise well to future clients | Predictions may be unreliable | Use cross-validation and test on unseen data |
| Time constraints may limit the depth of analysis | May not explore all features or models | Prioritise key features and models; document limitations |

---

### Actions

| Action | Timeline | Status |
|--------|----------|--------|
| Obtain and review historical client data from STADIOEquities | Week 1 | Not Started |
| Perform exploratory data analysis (EDA) to understand client patterns | Week 1-2 | Not Started |
| Clean and preprocess data (handle missing values, outliers, encode categories) | Week 2 | Not Started |
| Split data into training and testing sets (80/20 split) | Week 2 | Not Started |
| Train baseline models (Logistic Regression, Random Forest) | Week 3 | Not Started |
| Train advanced models (XGBoost) | Week 3 | Not Started |
| Evaluate model performance using accuracy, precision, recall, F1, AUC-ROC | Week 3 | Not Started |
| Identify top features predicting client dormancy | Week 4 | Not Started |
| Create visualisations (ROC curves, confusion matrices, feature importance) | Week 4 | Not Started |
| Document findings and provide recommendations for STADIOEquities | Week 4 | Not Started |
| Update README.md with all project documentation | Ongoing | In Progress |

---

### Assumptions

| Assumption | Impact if False |
|------------|-----------------|
| The historical data provided is accurate and complete | Analysis and predictions may be unreliable |
| Client behaviour patterns from the past 6 years will continue to be relevant | Model may not predict future dormancy accurately |
| Client ID is consistent across all datasets (funding, trading, app usage) | Unable to link client data across sources |
| Dormancy is defined correctly as no activity within 6 months | Wrong clients may be labelled as dormant |
| The data provided is sufficient to build a predictive model | May need additional features not currently available |

---

### Issues

| Issue | Date Identified | Impact | Resolution |
|-------|-----------------|--------|------------|
| No issues identified yet | - | - | Issues will be documented as they arise during the project |

---

### Decisions

| Decision | Rationale | Date Made |
|----------|-----------|-----------|
| Focus on dormancy within 6 months of registration | This is where the biggest increase (22% to 31%) was observed | Project Start |
| Use Python for analysis | Industry standard for data science projects | Project Start |
| Use 80/20 train-test split | Standard practice for model development | Project Start |
| Start with Logistic Regression as baseline | Simple, interpretable model to establish benchmark | Project Start |
| Use F1-Score as primary metric | Handles imbalanced data better than accuracy alone | Project Start |

---

### Dependencies

| Task | Depends On | Timeline |
|------|------------|----------|
| Data cleaning | Data being received from STADIOEquities | Week 2 |
| EDA | Data being cleaned | Week 2 |
| Model training | Data being split into train/test | Week 3 |
| Model evaluation | Model being trained | Week 3 |
| Feature importance analysis | Model being trained | Week 4 |
| Visualisations | Model evaluation being complete | Week 4 |
| Recommendations | All analysis being complete | Week 4 |
| Final README update | All tasks being complete | End of Project |
