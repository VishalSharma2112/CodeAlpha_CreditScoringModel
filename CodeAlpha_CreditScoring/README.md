# Credit Scoring Model using Machine Learning

## Project Overview

This project was completed as part of the CodeAlpha Machine Learning Internship.

The objective was to predict whether a customer is likely to default on their credit obligations using historical financial information. Since the dataset exhibited severe class imbalance, multiple machine learning models were evaluated using business-oriented metrics rather than relying solely on accuracy.

---

## Problem Statement

Financial institutions need to identify high-risk borrowers to minimize potential losses.

The goal of this project is to build a classification model that predicts whether a customer will default within the next two years.

Target Variable:

* `0` → Customer did NOT default
* `1` → Customer defaulted

---

## Dataset

Dataset: Give Me Some Credit (Kaggle)

Total Records: 150,000

Features Used:

* credit_utilization
* age
* late_30_59_days
* debt_ratio
* monthly_income
* open_credit_lines
* late_90_days
* real_estate_loans
* late_60_89_days
* dependents

Target Variable:

* default

---

## Exploratory Data Analysis (EDA)

Key Findings:

* The dataset was highly imbalanced:

  * 93.3% Non-default
  * 6.7% Default

* Defaulters were generally younger.

* Defaulters had lower monthly incomes.

* Historical late payments were strong indicators of future default.

* Multiple numerical variables exhibited skewness and extreme outliers.

* Delinquency variables showed strong multicollinearity.

---

## Data Preprocessing

The following preprocessing steps were performed:

* Removed customer_id
* Train-Test Split using stratification
* Prevented data leakage
* Median imputation for missing values
* Feature scaling for Logistic Regression
* Addressed class imbalance using class weights

---

## Models Evaluated

1. Logistic Regression
2. Balanced Logistic Regression
3. Decision Tree
4. Random Forest
5. Balanced Random Forest

---

## Model Performance

| Model                        | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| ---------------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression          | 93.4%    | 0.58      | 0.04   | 0.08     | 0.714   |
| Balanced Logistic Regression | 77.6%    | 0.18      | 0.67   | 0.29     | 0.802   |
| Decision Tree                | 89.8%    | 0.26      | 0.27   | 0.26     | 0.609   |
| Random Forest                | 93.6%    | 0.56      | 0.18   | 0.28     | 0.843   |
| Balanced Random Forest       | 92.4%    | 0.42      | 0.37   | 0.39     | 0.846   |

---

## Final Recommendation

Balanced Logistic Regression was selected as the preferred model.

Although it had lower overall accuracy, it achieved the highest Recall (67%), identifying the greatest number of actual defaulters.

In credit risk assessment, failing to identify risky borrowers can result in significant financial losses. Therefore, prioritizing Recall aligns more closely with business objectives.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## Project Structure

Credit-Scoring-Model/

├── data/

├── notebooks/

├── images/

├── README.md

├── requirements.txt

└── .gitignore

---

## Learning Outcomes

Through this project, I learned:

* The importance of preventing data leakage.
* Why accuracy can be misleading in imbalanced datasets.
* How to evaluate classification models using multiple metrics.
* The trade-offs between Precision and Recall.
* How business objectives influence model selection.

---

## Author

Vishal Sharma

CodeAlpha Machine Learning Internship
