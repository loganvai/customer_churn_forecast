📉 Telecom Customer Churn Prediction (TeleDom)
📌 Project Overview

This project focuses on predicting customer churn for a telecom operator “TeleDom”.
The company aims to proactively identify customers who are likely to cancel their subscription and offer them personalized promotions or retention strategies.

A machine learning model is developed using customer demographics, contract information, and service usage data to estimate the probability of churn.

🎯 Objective

Build a classification model that predicts whether a customer will terminate their contract, enabling the business to:

Reduce customer churn
Improve customer retention strategies
Optimize marketing and discount campaigns
📊 Data Description

The dataset consists of multiple sources merged by customerID:

📁 contract_new.csv
Contract type (monthly / yearly / 2-year)
Payment method
Billing type (paperless or not)
Monthly and total charges
Contract start and end dates
📁 personal_new.csv
Gender
Senior citizen status
Partner status
Dependents
📁 internet_new.csv
Internet service type (DSL / Fiber optic)
Online security
Backup services
Device protection
Tech support
Streaming TV and movies
📁 phone_new.csv
Multiple phone lines status
🧠 Project Pipeline
1. Data Loading
Imported and inspected all datasets
Checked missing values and data types
2. Exploratory Data Analysis (EDA)
Analyzed distributions of numerical and categorical features
Studied churn patterns across customer segments
Visualized relationships between features and target variable
3. Data Preprocessing
Handled missing values
Encoded categorical variables
Scaled numerical features
Created unified dataset using customerID
4. Feature Engineering
Created ContractDuration
Removed redundant or highly correlated features
Addressed class imbalance
5. Model Training

Models tested:

Logistic Regression
Decision Tree Classifier
LightGBM Classifier

Hyperparameter tuning performed using GridSearchCV.

🏆 Best Model

The best-performing model was:

🌟 LightGBM Classifier

Performance on test set:

ROC AUC: 0.89
Accuracy: 0.91
📈 Key Insights

Most important features influencing churn:

Contract Duration
Total Charges
Payment Method
Multiple Lines
Internet Service Type
⚠️ Error Analysis
False Negatives: 134 (customers who churned but were not detected)
False Positives: 31 (customers incorrectly predicted to churn)
Overall correct predictions: ~1500 customers
💼 Business Recommendations
🎯 Focus on retention campaigns for customers with short contract duration
💡 Provide personalized discounts and promotions for high-risk customers
📊 Monitor key churn drivers (charges, contract type, service usage)
📞 Improve service quality for underused services such as internet add-ons
🛠️ Technologies Used
Python
Pandas & NumPy
Matplotlib & Seaborn
Scikit-learn
LightGBM
Imbalanced-learn
Phik correlation analysis
📌 Project Structure
├── data/
│   ├── contract_new.csv
│   ├── personal_new.csv
│   ├── internet_new.csv
│   └── phone_new.csv
├── notebooks/
│   └── churn_analysis.ipynb
├── models/
├── README.md
🚀 Future Improvements
Apply SMOTE or advanced resampling techniques
Try XGBoost / CatBoost models
Deploy model as API (FastAPI / Flask)
Build dashboard for churn monitoring (Power BI / Streamlit)
👤 Author

Leonid
