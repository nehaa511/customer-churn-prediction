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

## Results
| Model | Accuracy | Precision (churn) | Recall (churn) | F1 (churn) |
|---|---|---|---|---|
| Logistic Regression | 0.74 | 0.51 | 0.78 | 0.62 |
| Random Forest | 0.80 | 0.65 | 0.51 | 0.57 |

Random Forest has higher accuracy, but Logistic Regression catches more churners (recall 0.78 vs 0.51). Since missing a churning customer is costly, Logistic Regression is the better fit here.

## Key insights
- About 27% of customers churned (class imbalance)
- Month-to-month contract customers churn more
- Customers with low tenure churn more

## Tech stack
Python, pandas, matplotlib, seaborn, scikit-learn

## Next steps
- Random Forest and XGBoost comparison
- Hyperparameter tuning
