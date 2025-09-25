Project Overview
This repository demonstrates housing price prediction using linear regression and advanced diagnostic techniques. The notebook implements a full workflow from data preprocessing, feature engineering, exploratory analysis, multicollinearity checks, residual diagnostics, to regularized models (Ridge and Lasso). It is optimized for interview readiness and provides clear visualizations and interpretable outputs.

Key Features
* End-to-end Linear Regression Pipeline:
  * Data cleaning (missing value imputation)
  * Categorical encoding (OneHotEncoder)
  * Numeric scaling (StandardScaler)
* Exploratory Data Analysis (EDA):
  * Target distribution plots
  * Pairplots for numeric features
  * Correlation heatmaps
* Regression Diagnostics:
  * Residual plots and Q-Q plots
  * Breusch-Pagan test for heteroscedasticity
  * Multicollinearity check using VIF
* Regularization Techniques:
 * Ridge and Lasso regression with **GridSearchCV** for hyperparameter tuning
* Model Evaluation:
 * MAE, MSE, RMSE, R² metrics on test set
  * Cross-validated R² scores
* Model Interpretation:
  * Coefficient tables with top features
  * Easy-to-understand impact of numeric features on target

Dataset
* Path: `/mnt/data/Housing.csv`
* Automatically detects the target column (`price`, `saleprice`, `median_house_value`, or last numeric column if not specified).
* Supports datasets with numeric and categorical features.

Workflow Summary

1. Load and inspect the dataset.
2. Conduct EDA, including distribution, pairplots, and correlation heatmap.
3. Preprocess data using a Pipeline:

   * Impute missing values
   * Scale numeric features
   * Encode categorical features
4. Split data into train-test sets.
5. Train a baseline Linear Regression model and evaluate.
6. Interpret coefficients and check multicollinearity with VIF.
7. Perform residual diagnostics: residual vs predicted plots, Q-Q plot, Breusch-Pagan test.
8. Apply Ridge and Lasso regularization with cross-validation.
9. Compare models and select the final model.
10. Save the trained model (`final_regression_model.joblib`) for deployment or reuse.
11. Produce interview-ready outputs, including top features and evaluation metrics.

Evaluation Metrics
* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² score (test set and cross-validated)

The notebook prints baseline vs regularized model performance, enabling comparison and final model selection.





This project is released under the MIT License.
