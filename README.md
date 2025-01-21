# Data Analysis and Forecasting

This project focuses on analyzing and forecasting temperature data in Latvia from 2018 to 2023. The analysis is performed using various time series analysis techniques and models.

## Project Overview

The project involves the following steps:

1. **Data Preparation**: Loading and preparing the temperature data from a CSV file.
2. **Time Series Analysis**: Performing various analyses on the time series data, including seasonal decomposition and autocorrelation plots.
3. **Model Training**: Training ARIMA and SARIMAX models on the temperature data to forecast future temperatures.
4. **Forecasting**: Using the trained models to predict future temperatures and visualizing the results.
5. **Validation**: Validating the forecast results using metrics like Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## Data Preparation

The initial data is loaded from a CSV file and prepared for analysis:

```python
import pandas as pd

# Load the data
temp = pd.read_csv("/tempo.csv")

# Change column names
temp.columns = ["Mēnesis", "Temperatūra"]

# Convert date column to datetime
temp["Mēnesis"] = pd.to_datetime(temp["Mēnesis"])

# Set date column as index
temp.set_index("Mēnesis", inplace=True)
```
