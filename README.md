# 🛫 AirPassengers Time Series Analysis
# 📌 Project Overview

This project analyzes and forecasts the number of monthly airline passengers using multiple time series forecasting methods.
The dataset shows the total number of international airline passengers from 1949 to 1960.

The main goal is to explore the trends, seasonality, and patterns of the data, and to compare the performance of different forecasting models.

# 📂 Dataset

Name: AirPassengers.csv

Source: Built-in classic dataset used in time series forecasting tutorials.

Columns:

Month — Monthly timestamps from 1949 to 1960

#Passengers — Number of airline passengers per month

# 🔍 Analysis Steps
# 1️⃣ Data Loading & Visualization

Loaded the dataset using pandas and visualized the time series.

Created both global and zoomed-in plots to observe short-term fluctuations and long-term trends.

# 2️⃣ Seasonal Decomposition

Decomposed the time series into:

Trend (overall direction)

Seasonality (recurring patterns)

Residuals (noise)

Observed a clear yearly seasonal pattern — peaks around July–August and lows in January.

# 3️⃣ Stationarity Check (ADF Test)

Used Augmented Dickey-Fuller (ADF) test.

The original series was non-stationary,
but became stationary after second-order differencing.

# 4️⃣ ARIMA Model

Built an ARIMA(1,1,1) model using statsmodels.

Evaluated residuals and generated a 12-month forecast with confidence intervals.

# 5️⃣ Holt-Winters Model

Applied Exponential Smoothing (multiplicative trend & seasonality).

Captured yearly patterns effectively and provided smooth forecasts.

# 6️⃣ Prophet Model (by Meta/Facebook)

Implemented Prophet, a modern forecasting model.

Automatically handled seasonality and produced interpretable components (trend, yearly seasonality, etc.).

# 📈 Results & Observations
Model	Key Characteristics	Comments
ARIMA	Captures autocorrelation and short-term dependencies	Requires differencing; sensitive to parameters
Holt-Winters	Handles trend and seasonality well	Smooth predictions, simple implementation
Prophet	Robust to missing data and outliers	Very intuitive and interpretable

# ✅ All models show an increasing trend in air passengers over time.
The peak months remain July–August, and the lowest demand is in January–February.

# 🛠️ Technologies Used

Python 🐍

pandas

matplotlib

statsmodels

prophet

Google Colab
