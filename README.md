# Credit Score Classification for Paisabazaar

## 📌 Project Overview
Paisabazaar, a financial services company, helps customers access loans and credit products.  
Credit score is a key metric for lenders to assess repayment capacity and manage risks.  
This project builds a **machine learning classification model** to categorize customers’ credit scores as **Good / Standard / Poor** using financial and behavioral data.

## 🎯 Objectives
- Clean and preprocess customer data (income, debt, loans, repayment history, etc.).
- Engineer features such as **Debt-to-Income** and **EMI-to-Income** ratios.
- Perform **exploratory data analysis (EDA)** to identify key trends.
- Build and evaluate ML models (**Random Forest, LightGBM, XGBoost**).
- Provide insights and recommendations for risk management.

---

## 📂 Dataset
- **File:** `dataset-2.csv`  
- **Records:** 100,000+  
- **Features:** Demographics, income, loan details, credit utilization, payment history.  
- **Target:** `Credit_Score` (Good, Standard, Poor)

Sensitive identifiers (`ID`, `Name`, `SSN`) were dropped to protect privacy.

---

## ⚙️ Steps in the Project
1. **Data Loading & Inspection**
   - View shape, columns, datatypes, missing values, and anomalies.
2. **Data Cleaning**
   - Handle missing values (median for numeric, mode for categorical).
   - Multi-hot encode `Type_of_Loan`.
   - Standardize categorical values.
3. **Feature Engineering**
   - Create `Debt_to_Income` and `EMI_to_Income`.
   - Encode categorical features (Label/One-hot encoding).
4. **Exploratory Data Analysis**
   - Univariate (distributions, histograms).
   - Bivariate (boxplots, relationships with `Credit_Score`).
   - Multivariate (correlation heatmap, pairplots).
5. **Model Building**
   - Train/test split (80/20).
   - Standardize numeric features.
   - Train Random Forest, LightGBM, XGBoost.
6. **Evaluation**
   - Accuracy, Macro F1, Classification Report.
   - Confusion Matrix.
   - Feature Importance visualization.
7. **Interpretation & Business Insights**
   - Identify top drivers of credit score (delayed payments, outstanding debt, utilization ratio).
   - Recommend actions for Paisabazaar.

---

## 📊 Results
- **Random Forest**: Robust baseline with good interpretability.  
- **LightGBM**: Best overall balance of accuracy and speed.  
- **XGBoost**: High recall on "Poor" credit score segment.  

**Key Features Driving Predictions**:
- Number of delayed payments  
- Outstanding debt  
- Credit utilization ratio  
- Annual income  
- Payment behavior  

---

## 🚀 Business Recommendations
- Flag customers with **frequent delayed payments** or **high debt-to-income ratio** as high-risk.  
- Offer **tailored financial products** (secured loans, low-interest options) to Standard/Poor categories.  
- Encourage **credit limit management and on-time payments** to improve customer scores.  

---

## 🛠️ Tech Stack
- **Python**: pandas, numpy, matplotlib, seaborn  
- **ML Models**: scikit-learn, XGBoost, LightGBM  
- **Environment**: Jupyter Notebook / Google Colab  

---

## 📁 Repository Structure
```
├── dataset-2.csv              # Dataset
├── Credit_Score_Template_Fixed.ipynb   # Main Notebook with full pipeline
├── README.md                  # Project Documentation
```

---

## ▶️ How to Run
1. Clone the repo or download the notebook and dataset.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open notebook:
   ```bash
   jupyter notebook Credit_Score_Template_Fixed.ipynb
   ```
4. Run all cells sequentially to reproduce results.

---

## 📌 Future Work
- Hyperparameter tuning for higher accuracy.
- Deployment via REST API or Chrome extension for real-time scoring.
- Integrating SHAP/LIME for model explainability.

---


