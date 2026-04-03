# 💳 Credit Risk Analytics & Machine Learning Framework

**Author**: Hardik Gupta  
**Project Focus**: Predictive Default Modeling & Loss Mitigation Strategy

## 🚀 Overview
This repository contains a dual-layer Credit Risk Analytics framework. It combines **Traditional Econometrics** (Rating Migrations, Expected Loss calculation) with **Advanced Machine Learning** (XGBoost, SHAP) to simulate the risk environment of a modern lending institution.

### Key Business Value:
- **Baseline Analysis**: Calculated Expected Loss (EL) for a 2,000+ account borrower cohort over 10 years.
- **Predictive Layer**: Deployed an XGBoost model achieving **87% accuracy (0.89 AUC)** in predicting defaults.
- **Economic Impact**: Identified a potential **₹65+ Cr loss reduction** opportunity through predictive early warning signals.

---

## 🛠 Tech Stack
- **Languages**: Python (Pandas, NumPy, Scikit-learn)
- **ML Frameworks**: XGBoost, Imbalanced-Learn (SMOTE)
- **Explainability**: SHAP (SHapley Additive exPlanations)
- **Visualization**: Matplotlib, Seaborn, Tableau

---

## 📂 Repository Structure
- `credit_risk_analysis.ipynb`: Traditional risk framework (PD, LGD, EAD, EL).
- `credit_risk_ML_model.ipynb`: **[NEW]** Machine Learning pipeline, simulation, and business impact.
- `Credit risk data.xlsx`: Comprehensive borrower cohort dataset.
- `requirements.txt`: Python dependencies.

---

## 🧠 Machine Learning Implementation Details
1. **Feature Engineering**: Derived 10+ predictive features including leverage-adjusted ROA and Macro-Stress Indices.
2. **Class Imbalance**: Utilized **SMOTE** to handle the minority default class, ensuring the model identifies high-risk borrowers effectively.
3. **Interpretability**: Used **SHAP Summary Plots** to explain model decisions to non-technical stakeholders (Consulting-centric approach).
4. **Validation**: 80/20 Stratified Split with ROC-AUC and Precision-Recall metrics.

---

## 📊 Sample Results: Business ROI
| Metric | Baseline (Traditional) | ML-Enhanced (Predictive) |
| :--- | :--- | :--- |
| **Identification Rate** | 65% (Rating-based) | **85% (XGBoost)** |
| **False Positives** | Higher | **Reduced by 22%** |
| **Mitigated Loss** | ₹0 Cr | **₹65.2 Cr** |

---

## 📦 How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/hardik00300/Credit-risk-analytics.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook:
   - Use Jupyter Lab or VS Code to open `credit_risk_ML_model.ipynb`.

---

## 🛡 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
