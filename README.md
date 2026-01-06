# austria-electricity-demand-forecasting
Monthly electricity demand forecasting for Austria using SARIMA with residual diagnostics and prediction intervals.

# Austria Electricity Demand Forecasting (SARIMA)

This project builds an end-to-end time series forecasting pipeline for
monthly electricity demand in Austria using classical statistical models.

## 📊 Dataset
- **Source:** Open Power System Data
- **Variable:** AT_load_actual_entsoe_transparency (MW)
- **Coverage:** Jan 2015 – Oct 2020
- **Original frequency:** Hourly
- **Modeling frequency:** Monthly (mean aggregation)

## 🎯 Objective
Forecast Austria’s electricity demand for the next 12 months and evaluate
classical baselines and SARIMA models.

## 🧠 Methodology
- Data cleaning & resampling (pandas)
- Exploratory analysis & rolling statistics
- Stationarity diagnostics (ADF, KPSS)
- Baseline models: Naïve, Seasonal-Naïve
- SARIMA model selection via AIC/BIC
- Residual diagnostics (ACF, Ljung–Box)
- 12-month forecast with prediction intervals

## 🏆 Final Model
**SARIMA(1,0,1)(1,0,0,12)**  
Selected based on:
- Lowest MAE on validation
- Well-behaved residuals
- Strong annual seasonality capture

## 📈 Results
- MAE: ~260 MW
- RMSE: ~297 MW
- sMAPE: ~3.7%
- Forecast shows clear winter peaks and summer troughs

## 🔮 Next Steps
- Add exogenous variables (temperature, holidays)
- Extend to SARIMAX
- Compare with ML-based time series models

## 🧑‍💻 Author
Jana Deghidy
