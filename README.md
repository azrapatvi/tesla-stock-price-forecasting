# 📈 Tesla Stock Price Forecasting using Prophet

## 🚀 Overview

This project focuses on forecasting stock prices of Tesla, Inc. using Facebook Prophet, a powerful time series forecasting model.

The goal is to analyze historical stock data and predict future trends while evaluating model performance.

---

## 📊 Dataset

* Source: Yahoo Finance
* Stock: Tesla (TSLA)
* Frequency: Daily stock prices
* Features used:

  * Date
  * Close Price

---

## 🛠️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* Prophet (Facebook Prophet)
* Plotly / Matplotlib

---

## ⚙️ Project Workflow

### 1. Data Collection

* Retrieved historical stock data using `yfinance`

### 2. Data Preprocessing

* Cleaned dataset
* Converted date column into proper datetime format
* Renamed columns to Prophet format:

  * `ds` → Date
  * `y` → Target variable (Close price)

### 3. Model Building

* Used Prophet for time series forecasting
* Trained model on historical data

### 4. Forecasting

* Generated future predictions
* Visualized trends and forecasted values

### 5. Evaluation

* Compared actual vs predicted values
* Observed model performance

---

## 📉 Results

* The model successfully captures the **overall upward and downward trend** of Tesla stock prices.
* Predictions are **smooth**, indicating strong trend learning.
* However, the model fails to capture **short-term fluctuations and volatility**.

### 📊 Actual vs Predicted Visualization

<img width="1919" height="909" alt="image" src="https://github.com/user-attachments/assets/f9e55197-76ac-453f-a376-205bed9781d1" />

## 📊 Model Evaluation

To better understand the performance of the model, actual stock prices were compared with predicted values (`yhat`).

### 🔍 Key Observations

* The model closely follows the **general trend** of the stock price.
* Predictions are **less volatile** compared to actual values.
* Sudden spikes and drops in stock price are **not captured effectively**.

### 📈 Interpretation

This behavior indicates that Prophet is effective for:

* Trend detection 📈
* Long-term forecasting

But less effective for:

* Short-term trading signals ⚡
* Highly volatile financial data

### 📋 Evaluation Data Sample

| Date       | Actual (Close) | Predicted (yhat) |
| ---------- | -------------- | ---------------- |
| 2025-03-18 | 225.31         | 250.22           |
| 2025-03-19 | 235.86         | 253.33           |
| ...        | ...            | ...              |


## ⚠️ Limitations

* Prophet struggles with highly volatile data like stock prices
* Does not account for external factors (news, market sentiment)
* Limited historical data reduces accuracy

---

## 🔮 Future Improvements

* Use advanced models like:

  * ARIMA
  * LSTM (Deep Learning)
  * Random Forest Regressor
* Add technical indicators (Moving Average, RSI, etc.)
* Increase dataset size for better performance

---

## 📌 Conclusion

This project demonstrates how time series forecasting can be applied to stock market data. While Prophet effectively models trends, it has limitations in handling market volatility.

---

## 📎 How to Run

```bash
pip install pandas numpy prophet yfinance plotly
```

```python
import yfinance as yf
from prophet import Prophet
```

