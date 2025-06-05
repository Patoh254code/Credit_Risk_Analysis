# 💳 Credit Risk Classification Analysis

[![Python](https://img.shields.io/badge/Python-3.13.3-blue.svg)](https://www.python.org/downloads/release/python-3133/)

# 📌 1.0 Overview

This project focuses on building a predictive model to assess credit risk. The goal is to use borrower data to classify whether a loan applicant is likely to default or repay their loan. This helps financial institutions reduce losses and make informed lending decisions.

# 🔍 2.0 Business and Data Understanding


### 🎯 Stakeholders

- **Loan officers**, **risk analysts**, and **credit managers** who need tools to assess risk more accurately.
- **Regulatory teams** who require transparent and interpretable credit models.
- **Data science teams** responsible for model development and monitoring.


### 🗂️ Dataset Description

- Historical loan records with borrower demographics, financial status, and loan outcomes from kaggle: https://www.kaggle.com/datasets/udaymalviya/bank-loan-data/data
- Key features include: 
    1. **Demographics**

       - `person_age`: Age of the applicant (in years).
       - `person_gender`: Gender of the applicant (male, female).
       - `person_education`: Educational background (High School, Bachelor, Master, etc.).

    2. **Financial**

       - `person_income`: Annual income of the applicant (in USD).
       - `person_emp_exp`: Years of employment experience.
       - `person_home_ownership`: Type of home ownership (RENT, OWN, MORTGAGE).

    3. **Loan Details**

       - `loan_amnt`: Loan amount requested (in USD).
       - `loan_intent`: Purpose of the loan (PERSONAL, EDUCATION, MEDICAL, etc.).
       - `loan_int_rate`: Interest rate on the loan (percentage).
       - `loan_percent_income`: Ratio of loan amount to income.

    4. **Credit History**
       - `cb_person_cred_hist_length`: Length of the applicant's credit history (in years).
       - `credit_score`: Credit score of the applicant.
       - `previous_loan_defaults_on_file`: Whether the applicant has previous loan defaults (Yes or No).

     5. **Target Variable**
        - `loan_status`: 0 if the loan was repaid successfully, 1 if the applicant defaulted.



### 📌 Project Goals

The primary objective is to develop a **predictive model** to:
- Identify **key drivers of loan default**
- Predict **likelihood of default** with ≥80% accuracy
- Prioritize **recall** to minimize missed defaulters (false negatives)
- Provide **interpretable outputs** for regulatory and policy alignment



### 📂 Project Structure

- `data`: Raw or sample dataset
- `notebook.pdf`: Summary of Jupyter Notebooks for EDA  and modeling
- `presentation.pdf`: Slide deck or final presentation
- `images`: Visualizations (ROC, confusion matrix, etc.)
- `requirements.txt`: List of required Python libraries
- `index.ipynb`: Main analysis notebook
- `README.md`: Project documentation 


### 🧪 Methods Used

- **Exploratory Data Analysis (EDA)**
  - Distribution analysis of default rates by demographic and loan attributes
  - Boxplots, countplots, correlation heatmap, pairplot

- **Data Preprocessing**
  - One-hot encoding (with `category_encoders`)
  

# 🤖 3.0 Modeling


- **Models used:**
     - **Logistic Regression**
     - **Decision Tree**
     - **XGBoost Classifier**

- **Techniques applied:**
     - **SMOTE** for handling class imbalance
     - **Hyperparameter Tuning** via GridSearchCV
     - **Train-test split** for validation
     - **MinMaxScaler** for normalization

- **Evaluation Metrics**
     - Precision, Recall, F1-score, Accuracy
     - **AUC-ROC Curve**
     - Confusion Matrix


# 📈 4.0 Evaluation


Models were evaluated using:
- **Precision**, **Recall**, **F1-Score**
- **Accuracy**
- **AUC (Area Under ROC Curve)**
- **Confusion Matrix** and **ROC Curve** visualizations



## ✅ Final Recommendation

### 💡 Recommended Model: **XGBoost with SMOTE for balancing**

| Metric     | Score |
|------------|-------|
| Accuracy   | 92.43% |
| Recall     | 82.78% |
| F1-Score   | 82.90% |
| AUC        | 97.57% |

> Chosen due to its **high recall**,high AUC and high accuracy, while maintaining **balanced operational usability** for overall credit decision-making.



### 📊 Key Visualizations

| Visualization                       | Sample |
|------------------------------------|--------|
| 📈 ROC Curve (Model Comparison)     | ![ROC](images/roc_curve.png) |
| 📊 Confusion Matrix (XGB + SMOTE)    | ![Confusion Matrix](images/conf_matrix_xg_sm.png) |
| 📌 Feature Importance (XGBoost + SMOTE) | ![Feature Importance](images/feature_importance.png) |



# ✅ 5.0 Conclusion


- **Default history**,**interest Rate**, **loan-to-income ratio**, and **persons income** were key predictors of default.
- **XGBoost + SMOTE** achieved the best overall performance.
- The model can be used to segment borrowers into risk groups for tailored credit strategies.



# 💻 How to Run This Project

1. **Clone the repo**
2. **Create a virtual environment (optional)**
3. **Install dependencies**
4. **Launch the notebook**

## 📌 Future Work
- Add more classification models for deeper comparison
- Deploy best model

## 👤 **Author**
📧 **Patrice Okoiti**-okoitipatrice96@gmail.com

🔗 **GitHub – @Patoh254code**




