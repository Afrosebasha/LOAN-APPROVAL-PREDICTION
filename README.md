# LOAN-APPROVAL-PREDICTION
oan Approval Prediction uses machine learning to assess loan eligibility based on income, credit history, and other factors. The Random Forest model delivers the best results, enabling real-time predictions. Future enhancements include ensemble learning and feature improvements.

# Loan Approval Prediction

## Project Overview

Loans play a crucial role in modern financial systems, contributing significantly to a bank’s overall profit. They help individuals manage education expenses, afford luxury items like houses and cars, and meet various financial needs. However, financial institutions must carefully evaluate applicants before approving loans, considering multiple factors such as income, credit history, and employment status.

This project aims to develop a machine learning model that predicts whether an applicant’s loan will be approved based on key background information, including gender, marital status, income, and credit history.

## Dataset Description

The dataset consists of several features that influence loan approval decisions:

- **Gender:** Some lending institutions may consider gender in loan approvals based on historical data or policies. If any gender-based discrimination exists, it could impact the approval process.
- **Marital Status:** Married individuals are often perceived as more financially stable, which may positively influence loan approval chances.
- **Dependents:** A higher number of dependents could indicate increased financial responsibilities, potentially affecting loan repayment capacity.
- **Education:** A higher level of education often correlates with better job prospects and financial stability, making graduates more likely to get loan approvals.
- **Self-Employed:** Self-employed individuals may experience irregular income patterns, leading to increased scrutiny from lenders.
- **Applicant Income:** Higher income usually indicates a greater ability to repay a loan. However, extremely high or low incomes may raise concerns for lenders.
- **Co-Applicant Income:** A co-applicant’s income supplements the household income, potentially improving loan eligibility.
- **Loan Amount:** Lenders assess whether the requested loan amount aligns with the applicant’s income and financial capacity.
- **Loan Term:** The loan tenure affects monthly repayment amounts. Shorter terms indicate quicker repayment, whereas longer terms may result in higher interest payments.
- **Credit History:** One of the most critical factors—applicants with a good credit history (1.0) are more likely to receive loan approval.
- **Property Area:** The property’s location (urban, rural, or semi-urban) can impact loan approval based on risk profiles and lending policies.

## Project Workflow

### 1. Data Preprocessing & Cleaning

- Handled missing values:
  - Numerical columns: Filled with mean/median.
  - Categorical columns: Filled with mode.
- Performed correlation analysis between categorical variables.
- Addressed skewness using logarithmic transformations on `total_income`, `loan_amount`, and `loan_amount_term` to normalize distributions.
- Encoded categorical variables into numerical representations.

### 2. Exploratory Data Analysis (EDA)

- Visualized relationships between key features.
- Identified patterns and trends in loan approvals.

### 3. Model Development

- **Train-Test Split:**
  - 75% training / 25% testing
- **Implemented machine learning models:**
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - K-Nearest Neighbors (KNN)

### 4. Handling Data Imbalance

During model evaluation, we observed significant class imbalance:

- **Loan Approved:** 422
- **Loan Not Approved:** 190

This imbalance led to misleading classification metrics due to oversampling. To address this, we applied **Random Over-Sampling**, which balanced the dataset by increasing the minority class samples.

### 5. Model Evaluation & Selection

- After balancing the dataset, we re-trained all models.
- **Random Forest performed best**, showing minimal differences in precision, recall, and F1-score, making it the optimal choice.

## Prediction Module

To test the model, a user-input table has been created, allowing users to enter relevant details and predict loan approval status in real time.

## Future Improvements

- Implement ensemble learning techniques to combine multiple models for improved accuracy and performance.
- Fine-tune hyperparameters to further optimize predictions.
- Enhance feature engineering by incorporating additional external financial data.

