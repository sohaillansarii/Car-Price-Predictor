

# Car Price Prediction

This repository explores used car price prediction across two distinct datasets (300 rows and 8,000+ rows). It compares traditional linear models against advanced tree-based ensembles and Optuna-based hyperparameter optimization.

---

##  Project Overview

### Model 1: Random Forest & XGBoost (Optuna-Tuned)

**Dataset:** `car_details.csv` (8,000+ rows)

This project focuses on maximizing prediction accuracy using tree-based ensemble models. The workflow includes:

* Data cleaning and preprocessing
* Regex-based feature extraction
* Label encoding of categorical variables
* Feature engineering
* Random Forest Regression
* XGBoost Regression
* Optuna Hyperparameter Optimization

### Model Performance

| Metric       | Random Forest | Basic XGBoost | Optuna-Tuned XGBoost |
| ------------ | ------------: | ------------: | -------------------: |
| **R² Score** |        0.9774 |        0.9799 |           **0.9812** |
| **MAE**      |     59,691.73 |     63,199.82 |        **56,405.55** |
| **RMSE**     |    118,801.89 |    111,989.16 |       **108,372.70** |

>  **Best Model:** Optuna-Tuned XGBoost achieved the highest R² Score and lowest prediction error.

---

##  Model 2: Linear & Lasso Regression

**Dataset:** `car data.csv` (300 rows)

A foundational machine learning project applying standard linear regression techniques to understand baseline predictive performance and feature selection through L1 regularization.

###  Model Performance

| Model             | R² Score |    MAE |
| ----------------- | -------: | -----: |
| Linear Regression |   0.8468 | 1.2217 |
| Lasso Regression  |   0.8468 | 1.2217 |

>  Although both models achieved identical R² and MAE values, Lasso Regression generated predictions that were marginally closer to the actual values in certain cases. Overall, the effect of L1 regularization on model performance was negligible.
---

## Requirements

Install all required dependencies using the provided `requirements.txt` file:

```bash
pip install -r requirements.txt

