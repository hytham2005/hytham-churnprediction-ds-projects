# Churn prediction
**Overview**

This project trains a machine learning model to predict customer churn for a telecom company. Keeping existing customers is often much better than trying to 
find new ones. Finding out the customers that are more likely to leave early can help the company take action before it is too late.

**Dataset**

The dataset that I used is Telco Customer Churn Dataset made by IBM, and it has 7043 records and 21 attributes related to a customer's profile characteristics,
account data, and subscribed services. The target variable is to find out whether the customer had churned or not.

**My work**

- I cleaned the dataset by handling missing values, removing duplicates, dropping unnecessary columns, and converting the datatype of TotalCharges column from string to float. 

- I scaled values of float columns between 0 and 1.

- I fixed the class imbalance issue since only 26% of customers actually churned.

- I compared two resampling techniques: SMOTE and SMOTEENN.

- I trained and evaluated three models: Logistic Regression, Random Forest, and XGBoost.

**Results**

| Model | Resampling | Recall | Precision | Accuracy |
|---|---|---|---|---|
| Logistic Regression | SMOTE | 75% | 52% | 75% |
| Random Forest | SMOTE | 54% | 58% | 78% |
| XGBoost | SMOTE | 51% | 58% | 77% |
| Logistic Regression | SMOTEENN | 85% | 46% | 70% |
| Random Forest | SMOTEENN | 75% | 51% | 74% |
| XGBoost | SMOTEENN | 74% | 52% | 75% |

**Best Model**

Logistic Regression with SMOTEENN got the best recall of 84%. I chose recall as the main metric because losing a customer who is about to churn is much worse
than mistakenly flagging one who stays.

**Tools**
-Programming Language: Python
-Libraries: Pandas, NumPy, Scikit-learn, Imbalanced-learn, XGBoost, Seaborn, Matplotlib.
