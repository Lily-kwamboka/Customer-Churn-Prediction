# Telco Customer Churn Prediction

This project aims to predict customer churn using the Telco Customer Churn dataset. Unlike earlier projects that focused on descriptive and inferential analysis, this one emphasizes predictive modeling to uncover patterns and provide actionable business recommendations.

---

##  Objective
Can we accurately predict which customers are likely to churn?

What are the most important factors driving customer churn?

Can we improve business decisions using these predictions?

Where does the model perform well — and where does it struggle?

How should the business intervene to reduce churn?



---

##  Tools & Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Logistic Regression
- Random Forest Classifier
- ROC Curve, Confusion Matrix, Precision/Recall/F1

---

##  Data Preprocessing

- Converted `TotalCharges` to numeric and handled missing values.
- Removed non-predictive columns like `customerID`.
- Encoded categorical variables using one-hot encoding.
- Split data into training and testing sets (80/20).

---

##  Modeling

### Logistic Regression (Baseline & Tuned)
- Achieved ~80–81% accuracy.
- Precision for churn: ~69%
- Recall for churn: ~56%
- F1-score for churn: ~62%
- ROC curve showed strong model performance over random guessing.

### Random Forest Classifier
- Used for identifying top predictive features via feature importances.

---

##  Key Predictive Features

Based on the Random Forest model:

| Feature                         | Importance |
|----------------------------------|------------|
| Tenure                          | 0.170      |
| Monthly Charges                 | 0.166      |
| Internet Service (Fiber Optic) | 0.036      |
| Electronic Check Payment        | 0.036      |
| Contract Type (Two Year)        | 0.035      |
| Online Security                 | 0.029      |
| Gender (Male)                   | 0.029      |
| Paperless Billing               | 0.026      |
| Partner                         | 0.024      |

---

##  Predictive Findings

- Customers with **short tenure** and **high monthly charges** are more likely to churn.
- Those using **electronic checks** or **fiber optic service** show higher churn rates.
- **Long-term contracts** and **online security features** help reduce churn.
- Slight demographic influence observed (e.g., gender, partner status).

---

##  Business Recommendations

- **Engage short-tenure customers** early with offers and loyalty programs.
- **Reevaluate high-charge plans** to improve value perception.
- **Survey fiber-optic users** to uncover service pain points.
- **Encourage auto-pay methods** and discourage electronic checks.
- **Promote two-year contracts** through discounts or loyalty points.
- **Bundle online security features** as a value-add to retain customers.

---

##  Files

- `INDEX.ipynb`: Full Jupyter Notebook with data analysis, model building, and evaluation.
- `README.md`: Project summary and key takeaways.

---

##  Future Work

- Experiment with ensemble models (e.g., XGBoost, Gradient Boosting).
- Apply SMOTE or class-weight balancing to improve recall on churn cases.
- Deploy as a web dashboard for real-time customer risk scoring.

---
