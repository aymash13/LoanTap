# 📊 LoanTap Creditworthiness Prediction  

## 📝 Problem Statement  
LoanTap is an online platform delivering customized loan products to millennials. The company aims to build an *underwriting layer* to determine the *creditworthiness* of individuals applying for personal loans.  

*Business Question:*  
- Should a credit line be extended to an applicant?  
- If yes, what repayment terms should be recommended?  

This project involves building a *Logistic Regression model* to predict loan repayment outcomes (loan_status) and provide *business recommendations* for safer lending decisions.  

---

## 📂 Dataset Overview  
The dataset (LoanTapData.csv) contains borrower details and loan-related information.  

### Key Features  
- *loan_amnt* – Loan amount requested  
- *term* – Loan term (36 or 60 months)  
- *int_rate* – Interest rate of the loan  
- *installment* – Monthly payment owed  
- *grade, sub_grade* – LoanTap-assigned credit grades  
- *emp_title, emp_length* – Employment details  
- *home_ownership* – Borrower’s homeownership status  
- *annual_inc* – Annual income (self-reported)  
- *verification_status* – Income verification status  
- *purpose* – Purpose of the loan (debt consolidation, home improvement, etc.)  
- *dti* – Debt-to-income ratio  
- *credit history attributes* – (earliest_cr_line, open_acc, revol_bal, pub_rec, etc.)  
- *loan_status (Target Variable)* – Loan repayment outcome  

### Engineered Features  
- *pub_rec_flag* – 1 if borrower has public record, else 0  
- *mort_acc_flag* – 1 if mortgage accounts > 0, else 0  
- *bankruptcy_flag* – 1 if bankruptcies > 0, else 0  

---

## 🔎 Project Workflow  

### 1. Exploratory Data Analysis (EDA)  
- Data structure & missing value analysis  
- Statistical summary of features  
- Univariate & Bivariate analysis (distribution plots, boxplots, correlation heatmaps)  
- Insights: loan amount trends, installment patterns, grade-wise repayment performance  

### 2. Data Preprocessing  
- Handling missing values  
- Outlier detection & treatment  
- Feature engineering (flags, ratio features)  
- Encoding categorical variables  
- Scaling numerical features (StandardScaler / MinMaxScaler)  

### 3. Model Building  
- Logistic Regression using *Scikit-learn* and *Statsmodels*  
- Coefficient interpretation & feature importance analysis  

### 4. Model Evaluation  
- Classification Report (Accuracy, Precision, Recall, F1-score)  
- Confusion Matrix  
- ROC-AUC Curve  
- Precision-Recall Curve  
- Tradeoff analysis (false negatives vs false positives)  

---

## 🛠 Tech Stack  
- *Python 3.10+*  
- *Pandas, NumPy* → Data wrangling  
- *Matplotlib, Seaborn* → Visualization & EDA  
- *Scikit-learn* → Modeling & evaluation  
- *Statsmodels* → Logistic regression interpretation  
- *Jupyter Notebook* → Development & documentation  

---

## ✅ Business Insights & Recommendations  
- Borrowers with *lower DTI* and *stable employment* are more likely to repay.  
- *Home ownership* and *higher annual income* correlate with safer borrowers.  
- Grades *A & B* are associated with higher repayment likelihood.  
- *Precision-Recall tradeoff* is critical:  
  - Focus on *Recall* → Identify real defaulters to reduce NPAs (non-performing assets).  
  - Maintain *Precision* → Avoid rejecting too many good borrowers.  
- Strategy: Adopt a balanced lending policy to minimize risk while sustaining approval rates.  

---

## 📌 Next Steps  
- Extend to *other ML models* (Random Forest, XGBoost) for performance comparison  
- Implement *threshold tuning* for business-optimized decision-making  
- Build a *dashboard (Streamlit / Flask)* for real-time loan application scoring
