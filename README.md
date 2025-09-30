# 📊 LoanTap Creditworthiness Prediction  

---

## 📝 Problem Statement  
LoanTap is an online platform that provides customized loan products to millennials.  
The company aims to build an **underwriting model** that determines the **creditworthiness** of individuals applying for Personal Loans.  

**Key Business Questions:**  
- Should a credit line be extended to a customer?  
- If yes, what repayment terms should be recommended?  

This project builds a **Logistic Regression model** to predict loan repayment outcomes (`loan_status`) and provide actionable business recommendations.  

---

## 🎯 Objective  
- Analyze borrower and loan attributes to understand repayment behaviors.  
- Build a predictive model to classify whether a borrower will **repay successfully or default**.  
- Extract business insights to guide **loan approval policies**.  

---

## 📂 Dataset Overview  

The dataset (`LoanTapData.csv`) contains borrower profiles and loan-related details.  

### Key Features  
- **loan_amnt** → Loan amount requested  
- **term** → Loan term (36 or 60 months)  
- **int_rate** → Interest rate of the loan  
- **installment** → Monthly payment owed  
- **grade, sub_grade** → LoanTap-assigned grades for creditworthiness  
- **emp_title, emp_length** → Employment details  
- **home_ownership** → Borrower’s homeownership status  
- **annual_inc** → Annual income (self-reported)  
- **verification_status** → Income verification status  
- **purpose** → Loan purpose (e.g., debt consolidation, home improvement)  
- **dti** → Debt-to-income ratio  
- **credit history attributes** → (earliest_cr_line, open_acc, revol_bal, pub_rec, etc.)  
- **loan_status (Target)** → Loan repayment status  

### Engineered Features  
- **pub_rec_flag** → 1 if borrower has public record, else 0  
- **mort_acc_flag** → 1 if mortgage accounts > 0, else 0  
- **bankruptcy_flag** → 1 if bankruptcies > 0, else 0  

---

## 🔎 Workflow  

1. **Exploratory Data Analysis (EDA)**  
   - Data structure & summary statistics  
   - Univariate & bivariate analysis (loan amount trends, grade distribution, default patterns)  
   - Correlation heatmaps  

2. **Data Preprocessing**  
   - Handling missing values  
   - Outlier treatment  
   - Feature engineering (flags, ratios)  
   - Encoding categorical variables  
   - Scaling numeric features  

3. **Model Building**  
   - Logistic Regression (Scikit-learn & Statsmodels)  

4. **Model Evaluation**  
   - Accuracy, Precision, Recall, F1-score  
   - Confusion Matrix  
   - ROC-AUC Curve  
   - Precision-Recall Curve  

---

## 📊 Model Performance  

| Metric            | Score |
|-------------------|-------|
| Accuracy          | ~82%  |
| Precision         | ~80%  |
| Recall            | ~78%  |
| ROC-AUC           | ~0.84 |

👉 The model shows good balance between **precision and recall**, making it reliable for minimizing loan defaults while not rejecting too many good borrowers.  

---

## 🛠 Tech Stack  
- **Python 3.8+**  
- **Pandas, NumPy** → Data wrangling  
- **Matplotlib, Seaborn** → Visualization & EDA  
- **Scikit-learn** → Model building & evaluation  
- **Statsmodels** → Logistic Regression interpretation  
- **Jupyter Notebook** → Development & documentation  

---

## ✅ Business Insights & Recommendations  
- Borrowers with **lower DTI** and **stable employment** are significantly more likely to repay.  
- **Home ownership** and **higher annual income** are strong repayment indicators.  
- Grades **A & B** correlate with safer lending.  
- Optimizing the **Precision-Recall tradeoff** is essential to reduce NPAs (non-performing assets).  
- Recommendation: Prioritize **Recall** to identify true defaulters, but balance with Precision to avoid rejecting too many potential customers.  

---

## 🚀 Future Improvements  
- Test advanced ML models (Random Forest, XGBoost, Gradient Boosting).  
- Apply **hyperparameter tuning** and **cross-validation**.  
- Build a **loan recommendation system** with repayment term suggestions.  
- Deploy via **Flask / Streamlit** for real-time credit scoring.  

---
