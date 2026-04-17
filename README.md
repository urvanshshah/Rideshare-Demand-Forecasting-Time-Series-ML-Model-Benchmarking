# Rideshare-Demand-Forecasting-Time-Series-ML-Model-Benchmarking
Rideshare Demand Forecasting : Time Series &amp; ML Model Benchmarking

Conducted an end-to-end time series demand forecasting study on the Capital Bikeshare dataset (Washington D.C., 17,379 hourly records, 2011–2012) benchmarking 4 models across statistical, machine learning, and deep learning paradigms as part of ASU's DSE 501 course.

• Performed comprehensive EDA across 17 features uncovering commuter peak demand at 8AM and 5–6PM on weekdays, seasonal ride variation (summer peak, spring trough), and non-linear relationships between temperature/humidity/windspeed and rental counts; validated findings via F-tests and two-sample t-tests (p-values as low as 3.97e-08).
• Engineered lag features (cnt_lag_1/2/3), extracted temporal attributes (hour, weekday, month), and implemented a temporal train-test split (year 0 → train, year 1 → test) to preserve time-series integrity across all models.
• Benchmarked 4 forecasting models: ARIMA (5,1,2), SARIMA (1,1,1)(1,1,1,24), LSTM (100 units, dropout, 24-step sequences), and XGBoost with GridSearchCV evaluated on MAE and RMSE; XGBoost outperformed all models with MAE 86.83 and RMSE 93.10, a 38% improvement over ARIMA baseline.
• XGBoost feature importance revealed lag features and hourly trends as the dominant predictors, with temperature and humidity as secondary environmental drivers informing actionable resource allocation strategies for peak vs. off-peak bike availability.

Tech: Python · XGBoost · ARIMA · SARIMA · LSTM · Pandas · NumPy · Matplotlib · scikit-learn · Statsmodels · Keras · Time-Series Forecasting · Hypothesis Testing
