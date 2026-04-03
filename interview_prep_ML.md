# Interview Prep Guide: Machine Learning for Credit Risk

### 🧠 1. Why XGBoost for Credit Risk? (Technical & Consulting View)
**Answer**: "For this project, I chose **XGBoost (eXtreme Gradient Boosting)** over a baseline like Logistic Regression for two reasons. 
- **Non-linear Relationship**: Credit risk factors (like ROA vs. Leverage) often have complex, non-linear interactions that linear models miss. 
- **Performance**: In my implementation, XGBoost achieved an **89% AUC-ROC**, significantly outperforming the 72% baseline of Logistic Regression.
- **Handling Missingness**: XGBoost handles missing data inherently, which is common in credit datasets. From a consulting perspective, it's the industry standard for high-performance predictive systems."

### ⚖️ 2. How did you handle the class imbalance (low default rates)?
**Answer**: "In credit data, defaults are usually 'rare events' (the minority class). To prevent the model from simply predicting 'No Default' for everyone, I used **SMOTE (Synthetic Minority Over-sampling Technique)**. 
- **Simple explanation**: Unlike traditional oversampling (which just duplicates rows), SMOTE creates *synthetic* examples of the minority class by interpolating between existing data points. This creates a balanced training set and forces the model to learn the specific characteristics of high-risk borrowers."

### 🔍 3. What do SHAP values mean in 'Plain English'?
**Answer**: "SHAP values provide **'local interpretability.'** While a model gives me a prediction, SHAP tells me *why* that specific prediction happened. 
- **The Story**: Imagine a borrower is flagged as high-risk. SHAP might show that their low ROA pushed the risk *up* by 20%, but their low Leverage pulled it *down* by 5%. 
- **Consulting Value**: It allows us to give CXOs a 'white-box' explanation for every loan decision, ensuring transparency and regulatory compliance."

### 🏢 4. How would this model be deployed in a real bank?
**Answer**: "This would typically be part of an **Early Warning System (EWS)**. 
- **Phase 1**: The model runs monthly on current loan accounts. 
- **Phase 2**: Accounts with a default probability > 0.70 are flagged for the Credit Monitoring team. 
- **Phase 3 (Consulting Recommendation)**: Instead of immediate default, the bank initiates **pre-default restructuring** (e.g., proactive refinancing), which is what saves the ₹65 Cr in my simulation."

### 📉 5. What are the limitations of this model?
**Answer**: "The biggest challenge in Credit ML is **Concept Drift**. If the macro environment changes suddenly (like a 2008 or 2020 event), the historical data might not reflect current reality. To mitigate this, I'd suggest implementing a **drift detection layer** and retraining the model on the most recent 12-month trailing windows."

### 📊 6. How did you quantify the ₹65 Cr loss reduction?
**Answer**: "I compared the **Baseline Expected Loss (EL)** of a ₹2,500 Cr portfolio (at 15% PD and 45% LGD) against a scenario where the ML model identifies high-risk borrowers with **85% recall**. 
- I assumed a **35% mitigation efficiency** (meaning if we intervene early, we save 35% of the potential loss through restructuring). The math works out to ₹65.2 Cr saved, representing a significant improvement in risk-adjusted returns."

---

### Tips for talking to Indus Insights (Consulting-Focused)
- **Emphasize ROI**: Always tie technical accuracy back to "₹ Crores saved."
- **Mention Stakeholders**: Talk about "presenting to the credit committee" or "explaining models to CXOs."
- **Focus on the 'So What?'**: A high AUC is good, but the *recommendation* (proactive intervention) is what consultants care about.
