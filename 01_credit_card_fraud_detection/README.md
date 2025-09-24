# Credit Card Fraud Detection

## 📌 Project Overview

This project focuses on detecting fraudulent credit card transactions using **Machine Learning** techniques.
It demonstrates handling **imbalanced data**, performing **exploratory data analysis (EDA)**, and applying multiple **classification models** to improve fraud detection.

---

## 🏦 Business Problem

Banks lose billions of dollars every year due to fraudulent credit card transactions. Fraud not only causes **financial loss** but also damages **customer trust**.
The challenge is that fraudulent cases are **extremely rare** (less than 0.2% of all transactions), making detection very difficult.

---

## 🎯 Goal

* Identify fraudulent transactions with **high recall** (catch as many frauds as possible).
* Reduce false negatives (missed frauds) that can cause heavy losses.
* Provide business insights into fraud patterns to help banks **prevent fraud proactively**.

---

## 🛠 Tools & Skills

* **Python** → Pandas, NumPy
* **Scikit-learn** → Logistic Regression, Random Forest, XGBoost
* **Imbalanced-learn** → SMOTE (Synthetic Minority Oversampling)
* **Matplotlib & Seaborn** → Data Visualization

---

## 📝 Approach

### 1. Data Exploration & Cleaning

* Dataset: [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
* 284,807 transactions → only 492 frauds (0.17%).
* No missing values.

### 2. Exploratory Data Analysis (EDA)

* Fraud cases are highly **imbalanced** compared to normal transactions.
* Fraud transactions tend to have **higher average amounts** than non-fraud.
* Fraud probability varies by **time of day (hourly patterns)**.

### 3. Data Preprocessing

* Created new **Hour** feature from the `Time` column.
* Applied **SMOTE** to balance the dataset:

  * Before SMOTE: Fraud = 492, Non-Fraud = 284,315
  * After SMOTE: Fraud = 284,315, Non-Fraud = 284,315

### 4. Modeling

Tested three ML models:

* **Logistic Regression** → 95% accuracy, good balance between precision & recall
* **Random Forest** → 100% accuracy (slight overfitting but strong results)
* **XGBoost** → 100% accuracy, stable results

### 5. Evaluation Metrics

* Used **Confusion Matrix**, **Precision**, **Recall**, **F1-score**, and **ROC-AUC**.
* High **recall** achieved, ensuring fraud cases were captured.

---

## 📊 Key Results

* **Logistic Regression**: Accuracy 95%, Recall 92%
* **Random Forest**: Accuracy \~100%, Recall \~100%
* **XGBoost**: Accuracy \~100%, Recall \~100%
* Fraud transactions are most likely to occur during **specific time windows** and with **larger amounts**.

---

## 💡 Business Insights

* Fraud detection systems should focus on **real-time transaction monitoring**.
* Banks can apply **stricter checks** during high-risk hours.
* Larger transactions should trigger **automatic verification** for security.

---

## 🏁 Conclusion

This project highlights the challenges of **fraud detection** with imbalanced data.
By applying **SMOTE** and **advanced ML models**, fraud can be detected with **very high recall**, helping banks reduce financial loss and protect customers.

## 📂 Dataset
- [Kaggle: Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
