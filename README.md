# Natural Gas Price Forecasting Project

## Objective
Analyze and forecast natural gas prices using time series data, with seasonality decomposition and signal detection for trading strategy insights.

## Data Processing & Feature Engineering
- Loaded dataset (Nat_Gas.csv) containing historical natural gas prices and dates.
- Parsed and extracted month, year, and month_name from the date column for seasonal analysis.
- Created a categorical month order to enable month-wise operations.
- Calculated the seasonal monthly average price and computed each point's deviation from its seasonal average.

## Signal Classification
Labeled each record as **Bullish**, **Neutral**, or **Bearish** based on deviation thresholds:
- **"Bullish"**: Price > seasonal average by >0.2
- **"Bearish"**: Price < seasonal average by <−0.2
- **"Neutral"**: Within ±0.2 of seasonal average

## Forecasting Model
- Used **Holt-Winters Exponential Smoothing** to fit a time series forecasting model to the natural gas prices.
- Produced 12-month forward price forecasts.

## Prediction Function
- Defined a reusable Python prediction function to estimate gas prices for any input date in the past or future (interpolates or uses the model forecast as required).

## Application
- Demonstrated prediction for both historic and future dates.
- Enables efficient scenario and what-if analysis for quantitative finance or energy markets.

## Conclusion
The notebook provides a complete time series workflow: preprocessing, feature extraction, signal labeling, robust statistical forecasting, and intuitive price prediction. Useful for data-driven trading signals, commodity risk assessment, and market forecasting use cases.
