HR Data Employment Retention Prediction
📌 Project Overview
Employee retention is a critical metric for organizational stability. This project utilizes a comprehensive human resources dataset to analyze patterns in workforce attrition. By integrating data analytics, machine learning, and visual storytelling via Tableau, we aim to transform raw HR data into actionable business insights.

❓ Problem Statement
Can employee retention be analyzed and predicted using a company's HR data? To answer this, the project focuses on two distinct objectives:

Prediction: Building a machine learning model to identify employees at risk of termination.
Diagnostics: Using visual analytics to understand the structural and environmental reasons why employees are leaving.
📂 Dataset
The analysis is based on a dataset containing 8,950 employee records with 15 variables covering demographics, job roles, compensation, and performance ratings.

Target Variable: Binary classification based on the termdate (termination date), distinguishing between "Active" and "Terminated" employees.
🛠️ Technologies & Tools
Python: Data cleaning, preprocessing, and machine learning (Pandas, NumPy, Scikit-learn, Imbalanced-learn).
Tableau: Interactive dashboarding for visual analytics and root cause analysis.
Jupyter Notebook: Code execution and documentation.
⚙️ Methodology
1. Data Preprocessing & Cleaning
Duplicate Removal: Ensured unique employee representation.
Feature Engineering: * Created a binary terminated variable (1 = Terminated, 0 = Active).
Calculated age and tenure from birth and hire dates.
Encoded categorical variables (One-hot and Ordinal encoding).
Data Validation: Verified outliers in salary and age as realistic workforce variations.
2. Predictive Modeling
Algorithm: Logistic Regression.
Class Imbalance Handling: Applied SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset (Active vs. Terminated).
Performance: The SMOTE-balanced model achieved higher recall and F1 scores, crucial for correctly identifying employees at risk of leaving.
Precision (Terminated): 0.62
Recall (Terminated): 0.75
3. Visual Analytics (Tableau)
An interactive dashboard was developed to validate machine learning predictions and identify root causes. View here: Tableau Dashboard

💡 Key Findings
Not Pay-Driven: Contrary to common assumptions, salary distributions between active ($70,992) and terminated ($70,860) employees are nearly identical.
No Demographic Bias: Gender and age show zero meaningful correlation with termination rates.
Departmental Churn: Attrition is heavily localized in Operations, Sales, and Customer Service. These departments exhibit a "hire-burnout-terminate" cycle, particularly visible in a massive spike of terminations for the 2017 hiring cohort.
Tenure: Tenure showed the strongest negative relationship with termination, indicating newer employees are at the highest risk.
🚀 Recommendations
Instead of broad, company-wide pay raises or diversity initiatives (which would yield low ROI), the organization should focus on targeted structural interventions:

Audit High-Churn Departments: Investigate management practices and workload in Operations and Sales.
Revamp Onboarding: Address the "hire-burnout" cycle by improving role clarity and support for new hires in high-volume roles.
