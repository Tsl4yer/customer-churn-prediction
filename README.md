# Customer Churn Prediction
> Stage 2 of the "Data-Driven Engineering & Decision Making" portfolio.

[![View Report](https://img.shields.io/badge/View-Live_HTML_Report-blue)](YOUR_GITHUB_PAGES_URL)
[![Python](https://img.shields.io/badge/Python-3.9+-yellow)]()

## Summary
Trained and compared Logistic Regression, Random Forest, and XGBoost
on 7,043 IBM Telco records to predict customer churn. XGBoost achieved
0.8364 ROC-AUC with 75.7% churner recall. Applied SHAP
explainability to identify the top business drivers of churn and
segmented customers into 4 risk tiers to enable targeted intervention.

## Key Findings
- Month-to-month contracts: 42.7% churn vs. 2.8% for 2-year contracts
- Median churned tenure: 10 months (vs. 38 months for retained)
- SHAP top drivers: `tenure`, `Contract_Two year`, `MonthlyCharges`
- 1,662 customers in Critical Risk tier (Total High+Critical net retention opportunity: $116,600)

## Results
| Metric | Value |
|--------|-------|
| XGBoost ROC-AUC | 0.8364 |
| XGBoost PR-AUC | 0.6467 |
| Churner Recall | 75.7% |
| Customers flagged (High+Critical) | 2,660 |

## Tech Stack
Python · pandas · scikit-learn · XGBoost · SHAP · Plotly · Quarto

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook notebooks/analysis.ipynb
