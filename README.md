
# 🟦 Loan Approval Prediction

### Machine Learning Classification Project | End-to-End Pipeline

---

## 📌 Project Overview

Banks receive thousands of loan applications daily. Approving the wrong customer increases financial risk, while rejecting good customers reduces business.

This project builds a complete **end-to-end loan approval prediction system** using machine learning.  
Given features such as:

- Income  
- Credit score  
- Employment experience  
- Loan amount  
- Loan percent income  
- Previous defaults  
- Loan intent  

the model predicts whether a loan should be **approved (1)** or **rejected (0)**.

---

## 📁 Dataset Information

**Target Variable:**
- **1 → Loan Approved**
- **0 → Loan Rejected**

**Key Features Used:**

- `person_age`
- `person_gender`
- `person_education`
- `person_income`
- `person_emp_exp`
- `person_home_ownership`
- `loan_amnt`
- `loan_intent`
- `loan_int_rate`
- `loan_percent_income`
- `cb_person_cred_hist_length`
- `credit_score`
- `previous_loan_defaults_on_file`

Dataset contains:
- Mixed categorical + numerical variables  
- Some imbalance  
- Noisy values in credit-related features  

---

## 🧭 Workflow

### **1️⃣ Data Understanding & Cleaning**
- Checked data types  
- Checked missing values  
- Converted categorical → numerical using Label Encoding  
- Verified all features became numeric  
- Removed inconsistencies  
- Split features (X) and target (y)  

---

### **2️⃣ Exploratory Data Analysis (EDA)**

Performed detailed EDA:

- Distribution of loan amounts, income, age  
- Countplots for categorical variables  
- Correlation heatmap  
- Outlier inspection  
- Approval rate across categories  

**Key insights:**

- Higher credit score strongly predicts approval  
- Loan percent income (EMI burden) influences risk  
- Previous defaults correlate with rejection  
- Income and education level affect approval likelihood  

---

### **3️⃣ Feature Engineering & Scaling**
- Label-encoded all categorical columns  
- StandardScaler applied for Logistic Regression  
- Created clean training/test splits  

---

### **4️⃣ Model Building**

Trained two models:

#### ✔ Logistic Regression (Baseline)
- Simple and interpretable  
- Lower recall and lower AUC  

#### ✔ Random Forest (Final Selected Model)
- Captures non-linear relationships  
- Strong performance  
- Works well with encoded categorical features  

---

## 📊 Model Performance

### **Final Random Forest Results**
- **Accuracy:** 0.93  
- **Precision (Approved = 1):** 0.89  
- **Recall (Approved = 1):** 0.76  
- **F1-Score:** 0.82  
- **ROC-AUC:** 0.9746  

The ROC-AUC of **0.9746** indicates excellent separation between good and risky customers.

---

## 🔥 Threshold Tuning (Advanced)

Tested thresholds: `0.5`, `0.4`, `0.35`, `0.3`, `0.25`  
Found that **0.35** gives the best balance for business use:

- Higher recall for approved customers  
- Minimal increase in false approvals  

Banks can adjust this threshold based on risk appetite.

---

## ⭐ Feature Importance

Top predictive features:

- **Credit Score**  
- **Loan Percent Income**  
- **Previous Loan Defaults**  
- **Loan Amount**  
- **Applicant Income**  
- **Employment Experience**  

This matches real-world lending policies.

---

## 🚀 Deployment-Ready Components

Saved files:

- `loan_rf_model.pkl`  
- `loan_scaler.pkl`  

Created a reusable function:

```python
predict_loan_status(model, scaler, input_data, threshold=0.35)
````

This makes the model usable in:

* APIs
* Loan approval dashboards
* Web applications
* Automated underwriting systems

---

## 🛠 Technologies Used

* Python
* Pandas, NumPy
* Scikit-Learn
* Seaborn & Matplotlib
* Jupyter Notebook

---

## 🎯 Key Learnings

* End-to-end ML workflow creation
* Encoding & preprocessing for mixed data types
* Feature importance interpretation
* Threshold tuning for business needs
* Creating production-ready ML pipelines

---

## 👨‍💻 Author

**Aliakbar Kanorewala**
Aspiring Data Scientist | Machine Learning Enthusiast
