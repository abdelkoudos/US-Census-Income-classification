# Income Prediction for U.S. Census Data

## Overview
This project aims to predict whether an individual earns more than $50K per year based on various social and economical features. The primary motivation is to understand the factors affecting income distribution, which can inform policy decisions. Additionally, this approach can be applied to credit scoring, where the prediction model helps identify financially stable individuals.

## Data
The dataset includes the following features:
- **Age**, **Workclass**, **Education**, **Occupation**, **Race**, **Gender**, **Capital Gain**, **Capital Loss**, **Hours per Week**, **Native Country**.
- **Target**: Income (0 = less than 50K, 1 = more than 50K).

## Data Cleaning

- **Missing Values**: Handled through imputation or removal.
- **Outliers**: Extreme values (e.g., hours worked per week) were cleaned to ensure data consistency.
- **Feature Encoding**: Categorical variables were one-hot encoded, and numerical features were standardized.
- **Removed income_value**: Highly correlated with target so it will lead to data leakage.

## EDA (Exploratory Data Analysis)
- **Chi-Square Test**: Evaluated relationships between categorical features and income.
- **ANOVA**: Analyzed how factors like education and age influenced income levels.
- **Correlation**: Investigated relationships between continuous features like age, capital gain, and income.

## Model
- **Algorithms Used**: Logistic Regression, Random Forest, and XGBoost.
- **Focus**: Reduced False Negatives (FN) by adjusting the decision threshold. This ensures that individuals with a higher probability of earning more than $50K (or creditworthy applicants) are less likely to be misclassified as earning less.

## Key Insights

- **Education** and **Capital Gain** were the most significant predictors of income.
- Policies to increase educational opportunities could help elevate incomes, especially in underserved areas.
- **Occupation** and **Work Class** also showed strong correlations with higher income.

## Results
- **Model Performance(test)**:
    - Random Forest: 75%
    - Random Forest: 80%
    - XGBoost: 81%
    - 
- **Evaluation Metrics**: The decision boundary was adjusted to minimize False Negatives (FN), as FN poses a higher risk of misclassification in credit scoring scenarios.

