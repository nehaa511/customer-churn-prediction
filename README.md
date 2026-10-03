# Customer Churn Prediction

Machine learning project to predict which telecom customers are likely to leave (churn).

## Dataset
IBM Telco Customer Churn dataset (7043 customers, 33 columns).

## What I did
- Exploratory data analysis (churn distribution, contract type, tenure, monthly charges)
- Data cleaning (fixed `Total Charges`, removed ID/location columns)
- Removed leakage columns (Churn Score, CLTV, Churn Reason, Churn Value)
- One-hot encoding, train-test split (80/20, stratified), scaling
- Baseline model: Logistic Regression with balanced class weights

## Results (Logistic Regression)
| Metric | Value |
|---|---|
| Accuracy | 0.74 |
| Recall (churn) | 0.78 |
| Precision (churn) | 0.51 |

## Key insights
- About 27% of customers churned (class imbalance)
- Month-to-month contract customers churn more
- Customers with low tenure churn more

## Tech stack
Python, pandas, matplotlib, seaborn, scikit-learn

## Next steps
- Random Forest and XGBoost comparison
- Hyperparameter tuning
