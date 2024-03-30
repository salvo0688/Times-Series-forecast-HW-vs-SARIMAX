
# Inventory Forecasting Project

## Overview

This project focuses on forecasting inventory levels using historical data, employing two different time series forecasting methods: Holt-Winters (HW) and Seasonal Autoregressive Integrated Moving Average with eXogenous variables (SARIMAX). The goal is to predict inventory for the year 2024, evaluating the models against actual data for 2023 to assess their performance.

## Approach

1. **Data Preparation**: We started by loading historical inventory and Cost of Goods Sold (COGS) data from an Excel file. The data included monthly records of inventory levels and COGS, spanning several years up to 2023, with some initial entries for 2024.

2. **Model Selection**: We chose two models for forecasting:
   - **Holt-Winters (HW)**: A method that accounts for level, trend, and seasonality in time series data.
   - **SARIMAX**: Extends the ARIMA model by incorporating seasonality and external variables (in this case, COGS), allowing for a more nuanced understanding of factors influencing inventory levels.

3. **Data Splitting**: We divided the data into training (up to 2022) and testing sets (2023) to evaluate the models' performance against actual data.

4. **Model Fitting and Forecasting**:
   - For **HW**, we fitted the model using the training data and forecasted inventory for 2023 and 2024.
   - For **SARIMAX**, we included COGS as an external variable, repeating the fitting and forecasting process.

5. **Evaluation**: We compared the 2023 forecasts from both models against actual data, using Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) as metrics to assess accuracy.

6. **Visualization**: Plots were created to visually compare the actual inventory levels with the forecasts, highlighting the models' predictive capabilities.

## Understanding the Models

- **Holt-Winters (HW)**: This model is suited for time series data with trends and seasonal patterns. It breaks down the data into three components: level (average value), trend (direction of data over time), and seasonality (repeating patterns or cycles), adjusting these components over time to forecast future values.

- **SARIMAX**: This model is a sophisticated version of ARIMA, designed for time series data that is influenced by external variables or has seasonal patterns. SARIMAX can model the effects of external factors (like COGS) on the time series of interest (inventory levels), providing a detailed understanding of how these factors impact future values.

## Conclusion

Both Holt-Winters and SARIMAX models offer valuable insights into future inventory levels, each with its strengths. Holt-Winters is simpler and effective for capturing basic trends and seasonality, while SARIMAX provides a more comprehensive analysis by considering external factors. The choice between them depends on the specific requirements and complexity of the forecasting problem at hand.
