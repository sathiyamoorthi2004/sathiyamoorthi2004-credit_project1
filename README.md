🏦 Credit Risk Prediction Project
LightGBM + XGBoost + SHAP + LIME + Fairness Analysis

(Dataset: cs-training.csv)








This project implements a complete Explainable Credit Risk Prediction System using the popular Give Me Some Credit dataset from Kaggle.

The goal is to predict whether a borrower will experience serious delinquency within the next 2 years.

This project includes:

✅ LightGBM (main model)
✅ XGBoost (comparison model)
✅ SMOTE balancing
✅ SHAP (global + local explainability)
✅ LIME (local explanations)
✅ Bias/Fairness analysis (Age groups)
✅ Complete artifact export (credit_output.zip)

This meets all requirements for an Explainable Credit Scoring ML Pipeline.

📁 Repository Structure
sathiyamoorthi2004-credit_project1/
│── README.md
└── credit_project1.py


All generated outputs will appear inside:  

🚀 How to Run the Project
1. Install Dependencies
pip install lightgbm xgboost shap lime imbalanced-learn joblib matplotlib pandas numpy scikit-learn

2. Download the dataset

Place the file cs-training.csv in the same folder as credit_project1.py.

3. Run the script
python3 credit_project1.py


Or specify custom paths:

python3 credit_project1.py --datafile cs-training.csv --outdir credit_output

📦 Output Files Generated

After running, you will get:

📈 Model Metrics

File: metrics.txt

AUC

Precision

Recall

F1 Score

Confusion Matrix

🤖 Model Artifacts

best_lgb.pkl

preprocessor.pkl

🔍 Explainability (SHAP + LIME)

shap_summary.png

shap_feature_importance.csv

⚖️ Fairness / Bias Analysis

bias_check.txt

🗂️ All Files in One ZIP

credit_output.zip

🧠 Model Overview
Modeling Workflow
Step	Description
Data Cleaning	Removes ID fields, high-missing columns
Preprocessing	Scaling + one-hot encoding
Balancing	SMOTE oversampling
Model	LightGBM tuned with RandomizedSearchCV
Explainability	SHAP + LIME
Fairness	Age-group bias check
📌 Final Model Performance

(From metrics.txt)

Metric	Score
AUC	0.8468
Precision	0.4750
Recall	0.2469
F1 Score	0.3249
Confusion Matrix
[[27448   547]
 [ 1510   495]]

🔎 Explainability Summary
Global SHAP Insights

Top predictors of default:

Revolving Credit Utilization

Number of 90-day late payments

Debt Ratio

Monthly Income

30–59 day delinquency frequency

Local Explanations

For 5 customers (high-risk, low-risk, borderline):

SHAP force plots

LIME feature contributions

Saved under credit_output/

⚖️ Bias / Fairness Check

Age groups analyzed:

≤ 30

31–45

46–60

60

bias_check.txt shows default rate differences.

📬 Final Notes

This project does not depend on Google Colab.

The Python script is clean, production-ready, and well-structured.

All required explainability artifacts are automatically generated.

Perfect for academic submission, ML courses, or real-world credit scoring demos.

credit_output/
credit_output.zip
