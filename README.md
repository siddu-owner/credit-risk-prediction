# 💳 Credit Scoring Model

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange?logo=scikit-learn)
![Gradio](https://img.shields.io/badge/Gradio-UI-green?logo=gradio)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-yellow?logo=googlecolab)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

> Predict an individual's creditworthiness using past financial data
> with Machine Learning classification algorithms.

---

## 📌 Project Overview

This project builds a **Credit Scoring Model** that predicts whether
a loan applicant is likely to **default or not** based on their
financial history and personal information.

---

## 🎯 Objectives

- Predict credit default risk (Binary Classification)
- Compare multiple ML models
- Handle class imbalance using SMOTE
- Deploy an interactive prototype using Gradio



## 📊 Dataset

Synthetic credit dataset with **10,000 records** and **14 features:**

| Feature | Description |
|---------|-------------|
| age | Applicant's age |
| income | Annual income |
| loan_amount | Requested loan amount |
| loan_tenure_months | Loan duration in months |
| avg_dpd_per_delinquency | Average days past due |
| delinquency_ratio | Ratio of delinquent payments |
| credit_utilization_ratio | Credit usage ratio |
| num_open_accounts | Number of active accounts |
| residence_type | Owned / Rented / Mortgage |
| loan_purpose | Home / Auto / Education / Personal |
| loan_type | Secured / Unsecured |
| debt_to_income | Engineered feature |
| loan_to_tenure | Engineered feature |
| risk_score | Engineered feature |

---

## ⚙️ Tech Stack

- **Language:** Python 3.10
- **Libraries:** Pandas, NumPy, Scikit-learn, Imbalanced-learn
- **Visualization:** Matplotlib, Seaborn
- **Prototype UI:** Gradio
- **Environment:** Google Colab

---

## 🧠 Models Used

| Model | Accuracy | ROC-AUC | F1-Score |
|-------|----------|---------|----------|
| Logistic Regression | ~75% | ~80% | ~72% |
| Decision Tree | ~82% | ~85% | ~79% |
| **Random Forest** | **~88%** | **~92%** | **~85%** |

✅ **Best Model: Random Forest**

---

## 📈 Evaluation Metrics

- ✅ Accuracy
- ✅ Precision
- ✅ Recall
- ✅ F1-Score
- ✅ ROC-AUC Score
- ✅ Confusion Matrix

---

## 🖥️ Gradio Prototype

Interactive web app where you can input:
- Personal details (age, income, residence)
- Loan details (amount, tenure, purpose)
- Credit history (DPD, delinquency ratio, utilization)

And get instant prediction:
- ✅ No Default / ❌ Default
- Confidence score
- Default probability
- Risk score

---

## 🚀 How to Run

### Option 1 — Google Colab
1. Open `credit_scoring_model.ipynb` in Google Colab
2. Run all cells in order
3. Launch Gradio app from the last cell

### Option 2 — Local
```bash
git clone https://github.com/yourusername/credit-scoring-model.git
cd credit-scoring-model
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn gradio
jupyter notebook credit_scoring_model.ipynb
```

---

## 📉 Key Insights

- **Risk Score** is the most important feature
- **Delinquency Ratio** and **Credit Utilization** are strong predictors
- SMOTE significantly improved recall for the minority class (defaulters)
- Random Forest outperformed all other models
