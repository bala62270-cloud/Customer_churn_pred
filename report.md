
# Project: Interpretable Machine Learning — SHAP Analysis of Customer Churn Prediction
*Date:* 2025-11-20 07:11

## 1. Objective
Build a binary classification model to predict customer churn and use SHAP to explain model predictions both globally and for selected customers.

## 2. Dataset
Synthetic telecom-style dataset with 5000 records. Features include age, tenure_months, monthly_charges, contract_type, num_complaints, num_services, etc.

## 3. Model
Algorithm: GradientBoostingClassifier (sklearn), tuned with GridSearchCV.
Best params: {'learning_rate': 0.05, 'max_depth': 3, 'n_estimators': 100}

## 4. Performance (on test set)
- Accuracy: 0.741
- AUC: 0.700
- F1-score: 0.105

## 5. Interpretability (SHAP)
- Global insights: see outputs/shap_beeswarm.png and outputs/shap_bar.png
- Selected customer analyses:
  - High-risk customer: outputs/shap_force_0.html, outputs/shap_waterfall_0.png
  - Low-risk customer: outputs/shap_force_1.html, outputs/shap_waterfall_1.png
  - Borderline customer: outputs/shap_force_2.html, outputs/shap_waterfall_2.png

### Key findings (example)
- Month-to-month contract increases churn risk significantly.
- High monthly charges and recent complaints are strong drivers of churn.
- Longer tenure reduces churn probability.

## 6. Business recommendations
1. Target month-to-month customers with retention offers.
2. Proactively resolve customer complaints to reduce churn.
3. Offer discounts for high monthly-charge customers at risk.

## 7. Files to submit
- churn_shap_project.ipynb (or .py)
- outputs/ folder with saved plots and model
- report.md (this markdown)

