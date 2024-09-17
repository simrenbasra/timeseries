# Microsoft Stock Forecasting Project

## Project Objective

The goal of this project is to apply timeseries forecasting methods to Microsoft (MSFT) stock data to predict the close price of stock for the next 7 days.

### Key Areas of Focus:

1. **Exploratory Data Analysis (EDA):**
   - Visualise and analyse stock data to better understand the data
   - Identify trends, seasonality and patterns 
   - Prepare data for forecasting (ensuring data is stationary, no missing dates/values and data is indexed by datetime index)

2. **Forecasting Models:**
   - Implement and assess baseline models and more advanced models
   - Evaluate the performance of each model using the following error metrics: **MSE**, **MAE**, **RMSE**, and **MAPE**.

3. **Exogenous Variables:**
   - Incorporate external factors, like interest rates and volume into the SARIMAX model to improve forecasting accuracy.
   - Analyse the impact of these external variables on stock price predictions.

4. **Time eries Cross-Validation:**
   - Use timeseries cross-validation to ensure there is no data leakage.
   - Perform predictions over different folds and evalaute the performance.

5. **Model Comparison:**
   - Compare and contrast the performance of baseline methods with ARIMA/SARIMAX models to understand the trade-offs between simplicity and complexity.

## Project Structure

### 1. Data Preparation

   - Load and preprocess MSFT stock data.
   - Handle missing values and dates.
   - Ensure data is stationary before moving to forecasting.

- **Outcome:** 
   - A clean, prepared dataset ready for forecasting.

### 2. Baseline Forecasting Models

   - Implement the following simple forecasting techniques: Mean, Naive, Seasonal Naive and Drift.
   - Evaluate their performance using timeseries cross-validation and performance metrics mentioned above.

- **Outcome:**
   - Baseline performance metrics for comparison with advanced models.
   - The Drift method performed best compared to other baseline methods.

### 3. Exponential Smoothing Models

   - Apply Simple, Double, and Triple Exponential Smoothing to capture trends and seasonality.
   - Evaluate the effectiveness of smoothing techniques.

- **Outcome:**
   - These models struggled with the high volatility in MSFT data. While they captured trends to some extent, they were not robust enough for accurate stock price forecasting.

### 4. Auto ARIMA and SARIMA Models

   - Use Auto-ARIMA to automate ARIMA, SARIMA and SARIMAX models and find the optimal parameters.
   - Prepare exogenous variables before adding them to the SARIMAX model and assess their effect on models predictions.

- **Outcome:**
   - ARIMA and SARIMA models showed better performance than baseline methods, capturing the seasonality and underlying trends in the data.
   - However, the high volatility of stock prices, combined with unpredictable events such as COVID-19 still proves challenging for these advanced models.


### Future Work and Next Steps
- **Feature Engineering:**
   - Instead of predicting Close price of stocks, perhaps move to predicting whether stockholders will see a return or not on their investment.

- **Advanced Models:**
   - Consider incorporating other models like XGBoost or *LSTM networks to see if they are able to handle volatile data better.
