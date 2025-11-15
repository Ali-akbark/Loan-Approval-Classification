# 🟦 **Loan Approval Prediction**

### **Machine Learning Project | Classification | End-to-End Pipeline**



## 📌 **Project Overview**

Financial institutions receive thousands of loan applications daily. Approving loans without proper evaluation increases the risk of default, while rejecting genuine applicants can reduce business.

This project builds a **machine learning model** to automatically predict whether a loan should be **approved or rejected** based on customer details such as:

* Income
* Credit history
* Employment
* Dependents
* Loan amount
* Property area

The goal is to create a reliable loan approval system that helps banks make data-driven decisions.



## 📁 **Dataset Information**

* Dataset Type: **Loan Approval Classification**
* Target Variable:

  * **1 = Loan Approved**
  * **0 = Loan Rejected**

Typical features include:

* ApplicantIncome
* CoapplicantIncome
* LoanAmount
* Loan_Amount_Term
* Credit_History
* Gender, Married, Education
* Self_Employed
* Property_Area
* Dependents

Dataset may include:

* **Missing values**
* **Categorical variables**
* **Outliers**
* **Imbalance between approved vs rejected**



## 🧭 **Workflow**

### **1. Data Understanding**

* Loaded dataset into Pandas
* Checked shape, columns, datatypes
* Analyzed missing values
* Detected categorical & numerical features
* Handled duplicates & basic cleaning



### **2. Exploratory Data Analysis (EDA)**

* Distribution plots (Income, Loan Amount)
* Countplots for categorical features
* Approval rate comparison across gender, property area, education etc.
* Boxplots for income vs loan approval
* Correlation heatmap

Key insights:

* Credit history strongly influences loan approval
* High applicant income increases approval chances
* Loan amount & loan term affect approval probability
* Married applicants had slightly higher approval ratios (dataset-dependent)



### **3. Data Preprocessing**

* Treated missing values with:

  * Median for numerical
  * Mode for categorical
* Encoded categorical variables using:

  * One-Hot Encoding
  * Label Encoding (for ordinal categories)
* Scaled numerical features using StandardScaler
* Addressed potential class imbalance using:

  * SMOTE
  * or Class Weights



### **4. Model Building**

Trained multiple models:

* Logistic Regression
* Random Forest
* Decision Tree
* XGBoost / Gradient Boosting (optional)

Used:

* Train-test split
* Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
* Cross-validation



### **5. Model Evaluation**

Evaluated models using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* ROC-AUC Curve

Focus:
✔ Improving recall for rejected loans
✔ Maintaining high precision for approved loans

Best performing model:
**Random Forest / Gradient Boosting** (dataset-dependent)



## 🚀 **How to Run the Project**

### **Clone the repository**

```bash
git clone https://github.com/yourusername/loan-approval-classification.git
cd loan-approval-classification
```

### **Install dependencies**

```bash
pip install -r requirements.txt
```

### **Run the notebook**

```bash
jupyter notebook
```

Open:
`loan_approval_prediction.ipynb`



## 🛠️ **Technologies Used**

* Python
* Pandas, NumPy
* Scikit-Learn
* Seaborn, Matplotlib
* Imbalanced-Learn (SMOTE)
* Jupyter Notebook



## 📌 **Key Learnings**

* Handling categorical variables
* Dealing with missing values properly
* Feature encoding strategies
* Imbalanced data techniques
* Model evaluation beyond accuracy
* Building an end-to-end ML classification pipeline



## 📄 **Future Enhancements**

* Deploy the model using Flask or FastAPI
* Convert the notebook into a modular Python application
* Build a front-end UI for loan application prediction
* Use SHAP values for model explainability
* Add more financial risk features



## 👨‍💻 **Author**

**Aliakbar Kanorewala**
Aspiring Data Scientist
Machine Learning | Data Analysis | Data Visualization






