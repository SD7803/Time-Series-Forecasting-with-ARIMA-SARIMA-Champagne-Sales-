# Time-Series-Forecasting-with-ARIMA-SARIMA-Champagne-Sales-

# 📈 Time Series Forecasting with ARIMA & SARIMA  
### Champagne Sales Forecasting (Perrin Frères Dataset)

---

## 🔍 Project Overview

This project focuses on **classical time series forecasting** using the well-known **Perrin Frères Monthly Champagne Sales dataset**.  
The objective is to analyze historical sales patterns, model trend and seasonality, and generate accurate forecasts using **ARIMA** and **Seasonal ARIMA (SARIMA)** models.

This project demonstrates **strong statistical foundations**, interpretability, and an end-to-end forecasting workflow .

---

## 🎯 Aim of the Project

- Analyze long-term **monthly champagne sales trends**
- Detect and handle **non-stationarity**
- Capture **seasonality in demand**
- Build and evaluate **ARIMA and SARIMA models**
- Validate assumptions using **ACF, PACF, and residual diagnostics**
- Forecast future sales with **confidence intervals**

---

## 🧠 Dataset Description

- **Dataset**: Perrin Frères Monthly Champagne Sales
- **Frequency**: Monthly
- **Target Variable**: Champagne sales volume
- **Time Span**: Multiple years of historical data

This dataset is widely used in forecasting literature due to its **strong seasonal patterns**.

---

## 🔬 Methodology

### 1️⃣ Exploratory Data Analysis (EDA)

- Visualized the raw time series to inspect:
  - Trend
  - Seasonality
  - Variance behavior

📌 **Observation**:  
The series shows an upward trend and strong annual seasonality → **non-stationary data**.

---

### 2️⃣ Stationarity & Differencing

Time series models like ARIMA assume stationarity.

- Applied **first-order differencing (d = 1)** to remove trend
- Applied **seasonal differencing (D = 1, lag = 12)** to remove yearly seasonality

📌 After differencing, the series fluctuates around a constant mean.

---

### 3️⃣ Autocorrelation Analysis (ACF & PACF)

#### 🔹 ACF (Autocorrelation Function)
- Measures correlation between observations at different lags
- Helps identify **MA (q)** terms

#### 🔹 PACF (Partial Autocorrelation Function)
- Measures direct correlation excluding intermediate lags
- Helps identify **AR (p)** terms

📌 These plots guided the selection of model parameters.

---

### 4️⃣ ARIMA Model

**ARIMA(p, d, q)** models:
- **AR (p)**: dependence on past values
- **I (d)**: differencing to achieve stationarity
- **MA (q)**: dependence on past errors

📌 ARIMA captures short-term dependencies but fails to fully capture seasonality.

---

### 5️⃣ Seasonal ARIMA (SARIMA)

To model repeating yearly patterns, we extend ARIMA to:

**SARIMA(p, d, q)(P, D, Q, s)**

- Seasonal AR & MA components
- Seasonal differencing
- Seasonal period **s = 12** (monthly data)

📌 SARIMA significantly improves model fit and forecast accuracy.

---

### 6️⃣ Model Diagnostics

To validate model assumptions:

- Residual time series plots
- ACF of residuals
- Normality and randomness checks

📌 Residuals behave like **white noise**, indicating a good model fit.

---

## 📊 Visualizations & Results

The project includes:
- Raw time series visualization
- Differenced series plots
- ACF & PACF plots
- Forecast vs actual values
- Forecast confidence intervals

📌 Forecasts successfully capture seasonal demand spikes.

---

## 🔮 Forecasting

- Generated **out-of-sample forecasts**
- Included **95% confidence intervals**
- Model captures:
  - Seasonal peaks
  - Stable long-term structure

---

## ✅ Conclusions

- Champagne sales exhibit **strong seasonality and trend**
- ARIMA alone is insufficient for seasonal data
- **SARIMA provides statistically robust forecasts**
- Classical time series models remain powerful and interpretable

---

## 🚀 Skills Demonstrated

- Time series EDA
- Stationarity analysis
- ARIMA & SARIMA modeling
- Statistical diagnostics
- Forecasting with uncertainty
- Python (pandas, statsmodels, matplotlib)

---

## 📌 Future Improvements

- Compare with **Holt-Winters / ETS**
- Introduce **exogenous variables (SARIMAX)**
- Benchmark against ML models (XGBoost, LSTM)
- Rolling-window cross-validation



⭐ If you found this project useful, feel free to **star the repository**!
