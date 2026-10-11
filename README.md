# Churn Risk Advisor v1.0

A web application designed to help telecom customer retention teams identify and prioritize customers at high risk of churning.

---

## Model card: Churn Risk Advisor v1.0

**Intended use:** rank existing telecom customers by churn risk so a retention team can prioritize calls. Decision support, not automation.
**Not for:** credit, pricing, or any decision that denies a service.
**Data:** IBM Telco Customer Churn, 7,043 customers, 26.5% churn.
**Model:** [e.g., Logistic Regression / Random Forest / XGBoost], chosen by 5-fold CV. Features: 30 encoded columns.
**Performance:** CV AUC [e.g., 0.84 +/- 0.02]; test AUC [e.g., 0.85] (test set used once).
**Threshold:** [e.g., 0.35], from a cost analysis (FN = PKR 6,000, FP = PKR 1,000).
**Limitations:** one US dataset from one period; no Pakistan data; associations, not causes; performance may drift as plans change.
**Fairness check (Week 15):** compare recall across gender and seniors.
**Owner and version:** Khuzaima Ahmed, v1.0, October 2026.

---

## Live Demo
🔗 **Live Application URL:** https://churn-risk-advisor-a2jrzbowteeqq3bbidptgt.streamlit.app/

---

## Screenshots

### One Customer
<img width="956" height="490" alt="image" src="https://github.com/user-attachments/assets/a6f1442e-6aa4-4808-aec3-8321e9f81f3f" />

### Batch Scoring
<img width="957" height="488" alt="image" src="https://github.com/user-attachments/assets/55bbb933-55d7-4f62-8105-def34d6e1bc1" />


---

## Project Notebooks (Weeks 1 - 3)

* **[Week 1: Exploratory Data Analysis & Data Cleaning](https://www.kaggle.com/code/khuzamasiddique/week-1/edit)**  
  * Exploratory data analysis, handling missing values, and initial data visualizations.
* **[Week 2: Building ML Models](https://www.kaggle.com/code/khuzamasiddique/week-2-building-ml-models/edit)**  
  * Encoding categorical features, feature scaling, and data pipeline setup.
* **[Week 3: Model Training, Evaluation & Hyperparameter Tuning](https://www.kaggle.com/code/khuzamasiddique/week-3-model-optimization/edit)**  
  * Training baseline models, cross-validation, performance evaluation (AUC, ROC), and threshold optimization.

---

## Deployment

To deploy this application live (using Streamlit Community Cloud):

1. Ensure your repository is pushed to GitHub with all required files (`app.py`, `churn_model.joblib`, `model_meta.json`, `requirements.txt`).
2. Go to [share.streamlit.io](https://share.streamlit.io/) and sign in with your GitHub account.
3. Click on **New app**.
4. Fill in your repository settings:
   * **Repository:** `Khuzama-tech/churn-risk-advisor`
   * **Branch:** `main`
   * **Main file path:** `app.py`
5. Click **Deploy!** Streamlit will automatically install the libraries from your `requirements.txt` and launch your app.

---

## How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Khuzama-tech/churn-risk-advisor.git](https://github.com/Khuzama-tech/churn-risk-advisor.git)
   cd churn-risk-advisor
