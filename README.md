# Fraud Detection Problem

In this project, **Machine Learning** is applied on a dummy transaction dataset to detect whether a transaction is fraudulent or not.

The shape of the dataset is **38,662 rows × 8 columns**.

The dataset consists of a target column **`label`** which has two categories:  
- `0` → Not fraud  
- `1` → Fraud  

It also has different feature columns containing transactional details listed below:

- **`accountAgeDays`** – The number of days the account has been active.  
- **`numItems`** – The number of items associated with the account.  
- **`localTime`** – Some measure of time, possibly in hours or a similar unit.  
- **`paymentMethod`** – The method used for payment (e.g., PayPal, store credit, credit card).  
- **`paymentMethodAgeDays`** – The number of days since the payment method was associated with the account (i.e., how long ago the current payment method was linked).  
- **`isWeekend`** – A binary indicator of whether the transaction occurred on a weekend (`1` for yes, `0` for no).  
- **`Category`** – The category of the transaction (e.g., electronics, shopping, food).  
- **`Label`** (Target column) – A binary label (`0` for legitimate, `1` for potentially fraudulent).  

---

## Goal  
The goal is to build a **classification model** that can accurately classify transactions as either legitimate or potentially fraudulent based on the given features.

---

## Machine Learning Lifecycle Followed  
```
Data Cleaning → Exploratory Data Analysis → Feature Engineering → Model Training → Hyperparameter Tuning
```

---

## Model Used  
A **RandomForestClassifier** was trained on the data.  
The final tuned model achieved a **recall of 1.00** on the test dataset.  

### Detailed Metrics  
- **For label `0`:**  
  - Precision: `1.00`  
  - Recall: `1.00`  
  - F1-score: `1.00`  

- **For label `1`:**  
  - Precision: `0.61`  
  - Recall: `1.00`  
  - F1-score: `0.76`  

---

## Handling Imbalanced Data  
- **Oversampling** the minority class using **Synthetic Minority Oversampling Technique (SMOTE)**.  
- The **objective function** for hyperparameter tuning was taken as `recall_score` for label `1` since **reducing false negatives** was the biggest concern.

---

## Libraries Used  

**Data Cleaning:**  
- `numpy`, `pandas`  

**Exploratory Data Analysis:**  
- `matplotlib.pyplot` (High-level API on Matplotlib), `seaborn`, `missingno`  

**Feature Engineering:**  
- `numpy`, `pandas`, `scikit-learn`, `feature-engine`  

**Model Training:**  
- `scikit-learn`  

**Hyperparameter Tuning:**  
- `optuna`  

---

⭐ **Feel free to star the repository if you like it!**  
📩 **Contact:** `rishabhpancholi134@gmail.com`
