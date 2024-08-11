
# 📈 Prediction of Stock Price Using Time Series Analysis


This repository contains a project for predicting stock prices using time series analysis. The primary model used in this project is the Auto ARIMA model, which helps in forecasting stock prices based on historical data. This project demonstrates the application of time series forecasting techniques and includes evaluation of prediction accuracy.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Data](#data)
- [Model Details](#model-details)
- [Error Analysis](#error-analysis)
- [Results](#results)
- [Contributing](#contributing)

## Project Overview

This project aims to predict future stock prices based on historical stock data using time series forecasting methods. The Auto ARIMA model is utilized to determine the best ARIMA parameters automatically and forecast future values.

## Installation

To run this project, you need to have Python and the following libraries installed:

- `pandas`
- `numpy`
- `statsmodels`
- `pmdarima` (for Auto ARIMA)
- `matplotlib`
- `scikit-learn` (optional, for additional metrics)

## Data

- **Data Columns:**
  - `Symbol`: The stock ticker symbol.
  - `Series`: The series identifier (e.g., EQ for equity).
  - `Prev Close`: The previous day's closing price.
  - `Open`: The opening price of the stock for the day.
  - `High`: The highest price reached during the day.
  - `Low`: The lowest price reached during the day.
  - `Last`: The last traded price before the market close.
  - `Close`: The closing price of the stock for the day.
  - `VWAP`: Volume Weighted Average Price.
  - `Volume`: The total number of shares traded.
  - `Turnover`: The total turnover for the stock.
  - `Trades`: The total number of trades executed.
  - `Deliverable Volume`: The volume of shares that were actually delivered.
  - `%Deliverble`: The percentage of deliverable volume out of the total traded volume.

- The dataset should be in CSV format and contain historical stock data with the above columns.

## Model Details

- **Model Used:** Auto ARIMA
- **Library:** `pmdarima`
- **Description:** The Auto ARIMA model automatically identifies the best ARIMA (AutoRegressive Integrated Moving Average) parameters based on the given dataset. It optimizes the selection of `p`, `d`, and `q` parameters by minimizing the AIC (Akaike Information Criterion) or BIC (Bayesian Information Criterion), resulting in a model that best fits the historical data.

## Error Analysis

The performance of the Auto ARIMA model is evaluated using the following metrics:

- **Mean Absolute Error (MAE):** `124.64`
  - This metric represents the average absolute difference between the predicted values and the actual values. It provides a measure of how far off the predictions are on average.

- **Root Mean Squared Error (RMSE):** `187.75`
  - This metric represents the square root of the average of the squared differences between the predicted and actual values. RMSE penalizes larger errors more heavily, offering a sense of overall prediction accuracy.

These error metrics indicate the model's accuracy in predicting the `VWAP` values. The MAE shows that, on average, the predictions are off by approximately `124.64`, while the RMSE suggests a larger variance in the errors, highlighting areas where the model may need further tuning.

## Results

The following graph shows the comparison between the actual `VWAP` values and the values forecasted by the Auto ARIMA model:

![Forecast vs Actual](https://github.com/user-attachments/assets/940d6b42-f38d-4dfd-9f10-02293a9e3994)


This visualization demonstrates the effectiveness of the model in predicting future stock prices, as well as areas where the model may need improvement.

## Contributing

Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please feel free to contribute. You can do this by:

- Submitting a pull request with your changes.
- Opening an issue to discuss potential enhancements or report bugs.

Please ensure that your contributions align with the project's goals and that your code follows the existing style and conventions. We appreciate your input and look forward to collaborating with the community!
