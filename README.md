# Air Passengers Time Series Analysis

This project performs **time series analysis and forecasting** on the **Air Passengers dataset** from Kaggle:  

---

## 📊 What is a Time Series?

A **time series** is a sequence of data points collected at regular time intervals.  
It allows us to analyse patterns, trends, and seasonality in data that depends on time.  
In this project, we are analysing monthly airline passenger counts to understand:
- How passenger numbers change over time  
- Whether there is a **trend** or **seasonality**
- How to build forecasting models to predict future values

---

## 📦 Dataset Description

The Air Passengers dataset contains the monthly number of airline passengers from **January 1949 to December 1960**.  
- Two main columns: `Month` and `#Passengers`  
- 144 records, each representing **one month** of passenger data :contentReference[oaicite:1]{index=1}

This dataset is commonly used for teaching and practicing **time series forecasting**.

---

## 🔍 What We Did

### 1. Time Series Visualization

We plot passenger counts over time to visually inspect:
- Trends (upward or downward movement)
- Seasonal patterns (yearly cycles)

---

### 2. Stationarity Testing

To apply many time series models, the data must be **stationary** (constant mean and variance over time).  
We perform tests such as the **Augmented Dickey-Fuller (ADF) test** to check stationarity.

Example (Python):

```python
from statsmodels.tsa.stattools import adfuller

result = adfuller(series)
print("ADF Statistic:", result[0])
print("p-value:", result[1])
# Time-Series-Analysis
```
### 3. ARIMA Model

ARIMA (AutoRegressive Integrated Moving Average) is a popular forecasting model that:

Models autocorrelation using lagged values

Uses differencing (I) to make the series stationary

Combines moving averages to capture error trends

### 4. SARIMAX Model

SARIMAX extends ARIMA with:

Seasonal terms (for yearly or monthly cycles)

Exogenous variables (optional additional predictors)
