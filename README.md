# Project Overview
The goal of this project is to develop a machine learning model to predict the scale of violent crimes across various US communities. By analyzing demographic, economic, and social factors, the models identify key predictors of safety and crime levels.

# Dataset
* Source: UCI Machine Learning Repository (Communities and Crime Data Set).
* Instances: 1,994 cities.
* Attributes: 100 predictive features (after cleaning) covering census and law enforcement data.
* Goal: Predict ViolentCrimesPerPop (normalized scale 0.0 - 1.0).

# Methodology and Project Flow
1. Data Preprocessing:
   * Removed non-predictive identifiers (community names, codes).
   * Filtered out columns with more than 50% missing values (mostly LEMAS data).
   * Handled remaining missing values using Median Imputation.
2. Model Training (75/25 Split):
   * Neural Network (MLP): To capture complex non-linear patterns.
   * Random Forest: To ensure stability and analyze feature importance.
   * XGBoost: For high-precision boosting performance.
3. Evaluation: Used MSE, MAE, and R-squared metrics to compare model performance.

# Key Visualizations
* Feature Importance: Identifies the top demographic drivers of crime.
* Actual vs. Predicted Plots: Visualizes how close the models guesses are to real-world data.
* Error Distribution: Analyzes the bias and variance of the Neural Network predictions.

# Conclusion
The models effectively predict crime trends, with ensemble methods (Random Forest/XGBoost) typically providing the most robust results. Demographic features like family structure and income levels were found to be the strongest predictors of community safety.

# Requirements
* pandas, numpy
* scikit-learn
* xgboost
* matplotlib, seaborn
