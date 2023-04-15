# Project Overview
The objective of this project was to analyze the electricity consumption per person data, which provides an estimate of power plant production minus losses, using time series analysis. The data was obtained from the World Bank and the International Energy Agency and covers the period from 1971 to 2014.

## Methodology
Python was used for all the analysis steps, including data cleaning, transformation, and modeling. Initially, an Augmented Dickey-Fuller (ADF) test was performed to determine if the time series was stationary. If the time series was non-stationary, transformations and differencing were applied to make it stationary.

Next, Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) plots were used to determine the order of the Autoregressive Integrated Moving Average (ARIMA) model. AIC was used to choose the best ARIMA model.

The residuals of the model were analyzed for white noise properties and autocorrelation. Engle's ARCH test and the Ljung-Box test were used to test for heteroskedasticity and autocorrelation, respectively.

## Results
The analysis indicated that the best model for this dataset was an ARIMA(1,1,1) with an AIC of 490.59. The residuals of the model showed white noise properties with no significant autocorrelation. The data did not exhibit significant heteroskedasticity.

## Project Structure
- [`data`](https://github.com/yacine-ammi/Algerian_Electricity_Consumption_Forecast/blob/main/Algeria%20electricity%20consumption%201971-2019.csv): contains the raw dataset
- [`notebook`](https://github.com/yacine-ammi/Algerian_Electricity_Consumption_Forecast/blob/main/electricity-consumption-forecast.ipynb): contains Jupyter notebooks for data preprocessing, EDA, and modeling.

# Conclusion
The time series analysis showed that the electricity consumption per person data was best modeled using an ARIMA(1,1,1) model. The residuals of the model showed white noise properties with no significant autocorrelation, and the data did not exhibit significant heteroskedasticity.
