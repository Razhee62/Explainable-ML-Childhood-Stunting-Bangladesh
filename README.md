# Explainable Machine Learning for Childhood Stunting Prediction in Bangladesh

## Project Overview

Childhood stunting is one of the major indicators of child health and nutrition status. This project applies statistical analysis and machine learning approaches to predict childhood stunting among under-five children in Bangladesh.

The project combines machine learning models with Explainable AI techniques to understand which factors contribute most to stunting predictions.

## Research Question

Can machine learning models predict childhood stunting among under-five children in Bangladesh, and which factors contribute most to the prediction?

## Dataset

Dataset:
Bangladesh Demographic and Health Survey (BDHS) Children's Recode Dataset

File:
BDKR81FL.DTA

The dataset includes:
- Child characteristics
- Maternal characteristics
- Household socioeconomic conditions
- Water and sanitation information

## Target Variable

Childhood stunting was defined using height-for-age z-score (HAZ):

HAZ < -2 SD = Stunted
HAZ >= -2 SD = Not stunted

## Methodology

1. Data Preparation
- Data cleaning
- Missing value handling
- Variable selection
- Feature preparation

2. Exploratory Data Analysis
- Distribution analysis
- Relationship exploration between predictors and stunting

3. Feature Engineering
- One-hot encoding for categorical variables
- Scaling of numerical variables

4. Model Development
Models used:
- Logistic Regression
- Random Forest
- XGBoost

5. Explainability
SHAP analysis was applied to Logistic Regression to interpret feature contributions.

## Model Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
| Logistic Regression | 0.614 | 0.325 | 0.601 | 0.422 | 0.673 |
| Random Forest | 0.762 | 0.457 | 0.083 | 0.140 | 0.630 |
| XGBoost | 0.744 | 0.378 | 0.145 | 0.210 | 0.642 |

Logistic Regression achieved the highest ROC-AUC and recall, making it the most suitable model for identifying stunting cases.

## Important Predictors

SHAP analysis identified:
- Maternal weight
- Child age
- Birth order
- Household wealth
- Maternal education
- Mother's age

as important contributors.

## Statistical Findings

Significant predictors included:
- Maternal weight (OR=0.960)
- Child age (OR=1.011)
- Birth order (OR=1.181)
- Higher maternal education (OR=0.476)
- Richest household wealth category (OR=0.473)

## Tools

Python libraries:
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Statsmodels
- Matplotlib
- Seaborn

## Limitations

- Cross-sectional data limits causal interpretation.
- Model performance depends on available survey variables.
- External validation was not performed.
- SHAP interpretation was performed for Logistic Regression.

## Future Improvements

- External validation
- More advanced explainable models
- Additional health-related variables
- Prediction dashboard development

## Author
Tayas Suk Imam Al Razee
Assistant Organizing Secretary
SUST Data Science Club
