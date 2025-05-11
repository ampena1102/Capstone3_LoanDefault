# 🏦 Loan Default Prediction Project

## Project Overview

This project focuses on predicting loan defaults using machine learning to support better lending decisions. The goal is to reduce risk for lenders while improving transparency for applicants and decision-makers. The work includes data cleaning, exploratory analysis, model development, performance evaluation, and business-aligned recommendations.

---

## Notebook Pipeline

1. **Data_Wrangling.ipynb**  
   - Cleaned raw data  
   - Imputed missing values  
   - Created features and mappings  
   - Exported cleaned dataset 

2. **EDA.ipynb**  
   - Explored class imbalance, loan purpose, regional patterns  
   - Highlighted early risk signals and potential biases

3. **Modeling.ipynb**  
   - Trained baseline and tuned models (LogReg, RF, XGBoost)  
   - Applied SMOTE and custom thresholding  
   - Evaluated performance with recall, F1, precision, AUC  
   - Performed error analysis to inspect model misclassifications

---

##Dataset Summary

- **Rows:** ~148,670  
- **Columns:** 39  
- **Target:** `status` (0 = Not Defaulted, 1 = Defaulted)  
- **Class Imbalance:**  
  - Not Defaulted: 112,031 (~75%)  
  - Defaulted: 36,639 (~25%)

---

## ✅ Final Model Summary

- **Model:** XGBoost Classifier  
- **Parameters:** Default (no hyperparameter tuning)  
- **Threshold:** 0.3 (custom threshold to increase recall)  
- **Features Used:** All cleaned + engineered features  
- **Performance (Test Set):**
  - Accuracy: 90%
  - Recall: 71%
  - Precision: 67%
  - F1-score: 69%
  - ROC AUC: 87%

---

## Key Predictive Features

- Loan-to-Value (LTV)  
- Debt-to-Income Ratio (DTI)  
- Income  
- Property Value  
- Credit Type (EQUI stood out and was retained after review)

---

## Business Use Cases

- **Loan Officers**: Risk score + key factors for each applicant  
- **Risk Managers**: Regional patterns for policy guidance  
- **Customer Service**: Clear explanation of denials  
- **Data Scientists**: Feature impact and model improvement

---

## Recommendations

1. **Deploy Explainable Risk Scoring**  
   Provide loan officers with SHAP-based insights alongside risk scores for transparency and accountability.

2. **Enhance Geographic Risk Monitoring**  
   Use model outputs to track high-default regions and propose policy interventions.

3. **Refine Features to Improve Stability**  
   Address outliers in income, loan amount, and DTI to reduce misclassification and increase trust.

4. **Future Work**  
   Test ensemble stacking, investigate model calibration, and reduce reliance on SMOTE by incorporating more real-world data.

---

## Data References

- Original dataset sourced from Kaggle  
- Mapping logic for loan purpose/type adapted from R-based work by a Kaggle participant  
- Fannie Mae guidelines and lending industry standards used for binning DTI and LTV ranges

---

## Author

Andrea M. Pena  

---
