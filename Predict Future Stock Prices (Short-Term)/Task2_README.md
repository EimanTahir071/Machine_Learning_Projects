```markdown
# Task 2 — Predict Future Stock Prices (Short-Term)

## Objective
Use historical stock data to predict the next day's closing price using features such as Open, High, Low, and Volume. Train a regression model and compare actual vs predicted values.

## Dataset / Source
- Stock data via Yahoo Finance using the `yfinance` library.
- Example ticker used in the notebook: `AAPL` (Apple).
- Adjustable period and interval (e.g., 3y, 1d).

## Notebook
- Filename: Task2_Stock_Prediction_notebook.py (Jupyter-style .py) or .ipynb

## Environment / Requirements
- Python 3.8+
- Key packages:
  - pandas, numpy
  - matplotlib, seaborn
  - scikit-learn
  - yfinance
  - joblib

Install:
pip install pandas numpy matplotlib seaborn scikit-learn yfinance joblib

## What this notebook does (step-by-step)
1. Downloads historical stock data for a chosen ticker via yfinance.
2. Performs feature engineering:
   - Return, HL_Pct, Open_Close_diff, MA5, MA10, etc.
3. Defines the target as the next day's Close price (shifted target).
4. Splits data chronologically (no shuffle) into train/test sets.
5. Scales numeric features and trains models:
   - RandomForestRegressor (default) and a baseline LinearRegression.
6. Evaluates using MAE, RMSE, and R2.
7. Plots actual vs predicted closing prices for the most recent window.
8. Shows residual distribution and feature importances.

## How to run
1. Ensure internet access for yfinance data download.
2. Open notebook and set parameters:
   - TICKER, PERIOD, INTERVAL
3. Run all cells:
   jupyter notebook Task2_Stock_Prediction_notebook.py

## Expected outputs / Deliverables
- Trained model saved (optional): stock_model_rf.joblib
- Evaluation metrics: MAE, RMSE, R2
- Plot of actual vs predicted closing prices
- Feature importance plot and analysis

## Tips & Extensions
- Add lag features (Close_t-1, Close_t-2 ...) to improve model context.
- Try time-series models (ARIMA, Prophet) or sequence models (LSTM) for alternate approaches.
- Use walk-forward validation for better time-series evaluation.

## Submission Checklist
- Notebook with detailed comments and explanation.
- README (this file).
- Model artifacts optional (joblib files).
- Push to GitHub and include repository link when submitting.
```