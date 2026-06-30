# time-series-decomposition-and-anomaly-detection-for-an-e-commerce-dataset

## Project Overview

This project analyzes an  -commerce dataset using time series analysis techniques to identify trends, seasonality, anomalies, and forecast future sales.

## Project Workflow

### 1. Data Preparation
- Loaded the dataset.
- Identified the required parameters:
  - **Date**
  - **Price**
  - **Quantity**

### 2. Date Indexing
- Converted the **Date** column into a DateTime format.
- Set the **Date** column as the dataset index.

### 3. Classical Time Series Decomposition
Used `statsmodels.tsa.seasonal_decompose` with an **additive model** and a seasonal period of **52 weeks** to decompose the time series into:
- Trend
- Seasonal
- Residual

The decomposition components were visualized in a single figure with a shared x-axis.

### 4. STL Decomposition
Performed **STL (Seasonal Trend decomposition using Loess)** and compared its performance with the classical decomposition method.

### 5. Anomaly Detection
Analyzed the residual component to identify anomalies present in the dataset.

### 6. Time Series Forecasting
Built a **SARIMA(1,1,1)(1,1,1,52)** model using approximately **2.5 years** of weekly data and forecasted the remaining weeks.

### 7. Model Evaluation
The forecasting model achieved the following performance metrics:

| Metric | Value |
|--------|-------:|
| MAPE | **68.06%** |
| RMSE | **1934.78** |

