# Daily Financial Return Prediction

*Kaggle Hull Tactical Challenge*

This project was completed as part of an MSc in Finance with Machine Learning, specifically for the *Introduction to Machine Learning* module. 

The dataset and problem formulation are drawn from the Kaggle Hull Tactical Challenge, which focuses on predicting daily financial returns using high-dimensional, noisy financial data.

**1. Data Preparation**
- Handling missing values and inconsistent observations
- Preserving the temporal structure of the data to prevent information leakage

All preprocessing steps were applied using training data only, with test data kept strictly out-of-sample.

**2. Feature Engineering**
To extract informative signals from noisy financial data, feature engineering included:
- Rolling window statistics (e.g. means and volatility measures)
- Lagged predictors to capture temporal dependence
- Normalisation and scaling based on historical information only
Feature construction was carefully designed to avoid look-ahead bias and to reflect only the information that would have been available at each point in time.

**3. Model Selection and Training**
Supervised machine learning models were trained to predict daily financial returns.

The focus was placed on regularised linear models to balance predictive power and interpretability, including:
- Lasso
- Ridge
- Elastic Net
- XGBoost
- Decision Trees
- Random Forest

These models were selected to mitigate overfitting in a high-dimensional setting and to provide insight into which features contributed to the predictions.

**4. Validation Strategy**
Model performance was evaluated using time-series cross-validation, implemented through a walk-forward or expanding window approach.

This ensured that:
- Training always preceded testing in time
- No future information was used in model estimation
- Performance estimates reflected realistic out-of-sample behaviour
- Random train–test splits were deliberately avoided.

**5. Evaluation and Interpretation**
Models were assessed using both statistical and financial evaluation criteria:
- Statistical accuracy metrics (MAE, RMSE, R²)
- Risk-adjusted return measures to assess economic relevance

**6. Reflection and Limitations**
The final stage involved analysing model limitations and sources of performance degradation.

Key observations included:
- Predictive signals were weak and unstable across time
- Feature engineering improved fit but did not guarantee economic profitability
- Proper validation substantially reduced apparent performance

These findings underscore the inherent challenges of applying machine learning to financial return prediction and emphasise the importance of realistic evaluation.
