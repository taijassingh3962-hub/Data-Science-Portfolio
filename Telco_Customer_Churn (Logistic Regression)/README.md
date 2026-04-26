# 📊 Customer Churn Prediction using Logistic Regression

## 📌 Project Overview
This project focuses on predicting **customer churn** (whether a customer will leave the service or not) using machine learning.  
Customer churn prediction is important for telecom companies because it helps identify customers who are likely to leave, so the company can take retention actions.

The dataset contains customer demographics, service usage, contract type, billing details, and payment information.

---

## 🎯 Objective
- Understand the dataset structure and churn distribution
- Clean and preprocess the data for machine learning
- Perform EDA to find key churn-related patterns
- Build a Logistic Regression model to predict churn
- Evaluate the model using classification metrics
- Improve churn detection using threshold tuning

---

## 📂 Dataset Features
The dataset includes the following columns:

- **Customer Info:** `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- **Account Info:** `tenure`
- **Services:** `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`
- **Billing & Contract:** `Contract`, `PaperlessBilling`, `PaymentMethod`
- **Charges:** `MonthlyCharges`, `TotalCharges`
- **Target:** `Churn` (Yes/No)

---

## 🛠️ Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 🧠 Machine Learning Approach

### 🔹 Algorithm Used
- **Logistic Regression** (Binary Classification)

### 🔹 Data Preprocessing
- Converted `TotalCharges` to numeric values
- Removed rows with missing `TotalCharges` (11 records)
- Dropped `customerID` (not useful for prediction)
- One-hot encoding for categorical features
- Feature scaling using `StandardScaler`
- Stratified train-test split due to class imbalance

---

## 📊 Exploratory Data Analysis (EDA)
Key insights from EDA:
- The dataset is **imbalanced** (around 73% No churn, 27% Yes churn)
- Customers with **low tenure** are more likely to churn
- **Month-to-month contracts** show higher churn
- Higher **MonthlyCharges** tend to increase churn probability

---

## 📈 Model Evaluation
The model was evaluated using:
- Accuracy
- Confusion Matrix
- Precision, Recall, and F1-score

Since the dataset is imbalanced, F1-score was important to measure churn prediction quality.

---

## 🎯 Threshold Tuning
Logistic Regression predicts churn probability.  
Instead of using the default threshold (0.5), threshold tuning was applied.

- Best threshold found: **0.4**
- This improved the balance between precision and recall for churn customers.

---

## 🔮 Model Usage (Prediction)
To predict churn for a new customer:
1. Apply the same preprocessing (encoding + scaling)
2. Predict churn probability
3. Use threshold **0.4** for final churn classification

Example logic:

- If `churn_probability >= 0.4` → Predict **Churn = Yes**
- Else → Predict **Churn = No**

---

## ✅ Conclusion
This project demonstrates a complete classification pipeline for churn prediction, including data cleaning, EDA, feature preprocessing, model training, evaluation, and threshold tuning.  
Logistic Regression provided a strong baseline model, and threshold tuning improved churn detection performance for real-world business use.

---

## 📌 Project Status
- ✔️ Completed  
- ✔️ Ready for portfolio and freelancing use  
