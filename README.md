# Linear Regression on California Housing Dataset

This project uses linear regression with different regularization techniques to predict housing prices in California. It compares the performance of Elastic Net and Ridge Regression using `SGDRegressor` from scikit-learn, with proper scaling and evaluation via cross-validation.

## Dataset

- **Source:** California Housing Dataset from `sklearn.datasets`
- **Target Variable:** Median House Value
- **Features:** Demographic and geographic indicators (e.g., median income, house age, latitude, longitude)

## Problem Statement

The goal is to evaluate how different regularization strategies affect the predictive accuracy of a linear regression model trained to estimate median housing prices. This type of problem reflects common tasks in real estate analytics, urban planning, and economic forecasting.

## Approach

The following steps were taken:

1. **Data Standardization:** Used `StandardScaler` to normalize input features for better gradient descent performance.
2. **Modeling:**
   - Applied `SGDRegressor` with:
     - Penalty set to `'elasticnet'` (combines L1 and L2 regularization)
     - Penalty set to `'l2'` (Ridge Regression)
3. **Evaluation:**
   - Performed **5-fold cross-validation** on both models
   - Compared mean validation scores to determine which approach performs better on this dataset

## Results

Both models were successfully trained and evaluated. The comparison showed how regularization affects model generalization and overfitting in practice.

## Transferable Skills Demonstrated

- Applied data preprocessing and model regularization techniques
- Implemented cross-validation to ensure robustness
- Compared models to make data-informed decisions
- Wrote reproducible code using scikit-learn and Python best practices

## Future Improvements

- Scale the project to larger and more complex datasets (e.g., Zillow data, geospatial data APIs)
- Add feature engineering techniques (log transformations, interaction terms)
- Use visualization tools to identify regional trends in housing prices
- Wrap the solution in a Streamlit or Flask app to simulate a real-world use case

## Tools Used

- Python
- scikit-learn
- NumPy, Pandas
