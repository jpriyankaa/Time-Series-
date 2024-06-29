# Time Series EDA and Stock Analysis of Tesla (2010-2024)

This project involves performing an Exploratory Data Analysis (EDA) and a comprehensive stock analysis of Tesla Inc. (TSLA) from June 29, 2010, to June 25, 2024, utilizing various Python libraries such as `yfinance` for data retrieval, `pandas` for data manipulation, `datetime` for date and time operations, and `matplotlib` for data visualization.

#### Data Retrieval and Overview
The project begins with fetching Tesla’s historical stock data using the `yfinance` library. This dataset includes key financial metrics such as Open, High, Low, Close, Adjusted Close prices, and Volume of shares traded. Initial inspection of the dataset is performed by displaying the first few and last few rows of the data to understand its structure.

#### Exploratory Data Analysis (EDA)
1. **Visualization of Historical Data**:
    - Entire dataset is plotted to visualize the trend of Tesla’s stock prices over the 14-year period.
    - Separate plots for the highest and lowest stock prices on each trading day are created to analyze the fluctuations and trends.

2. **Date-Specific Data Extraction**:
    - Data for specific periods, such as from January 1, 2021, to September 1, 2022, is extracted and visualized to focus on recent trends.
    - Date-specific opening prices are plotted to analyze stock performance over the selected period.

3. **Data Information and Manipulation**:
    - Detailed information about the dataset, such as data types and memory usage, is obtained.
    - The date column is reset and set as an index multiple times for different analyses.

4. **Datetime Operations**:
    - The `datetime` module is used to display current date and time, extract specific date components (year, month, day, weekday), and perform date-related operations.

#### Time Resampling
Time resampling techniques are applied to the dataset to facilitate analysis at different time intervals:
1. **Annual Resampling (Rule 'A')**:
    - Annual minimum and maximum values of stock prices are computed to summarize Tesla’s yearly performance from 2010 to 2024.

2. **Quarterly Resampling (Rule 'QS')**:
    - Data is resampled at the start of each calendar quarter to evaluate stock performance at the beginning of each quarter.

3. **Business Year End Resampling (Rule 'BA')**:
    - Data is aggregated at the end of each business year to review Tesla’s fiscal year-end financial metrics.

4. **Business Quarter Start Resampling (Rule 'BQS')**:
    - Data is aggregated at the start of each business quarter to analyze stock performance at the beginning of each fiscal quarter.

#### Key Findings
- The stock prices of Tesla have shown significant growth and fluctuations over the 14-year period.
- The highest stock price recorded was in 2021, reflecting Tesla’s peak market performance.
- Resampling the data provides insights into Tesla’s performance at different time intervals, aiding in understanding long-term trends and quarterly variations.

### Conclusion
The project effectively demonstrates the use of EDA and time series analysis techniques to understand and visualize Tesla’s stock performance over time. By leveraging Python libraries and financial data, meaningful insights are derived, which can be valuable for investors and analysts in making informed decisions.

  

# Time Series Analysis of Nvidia Stock and Airline Passengers Data

## 1. Introduction
- This project involves time series analysis of two datasets: Nvidia (NVDA) stock prices and airline passengers data. The aim is to perform various statistical analyses and model predictions using techniques like moving averages, exponential moving averages, ARIMA, and SARIMA models.

## 2. Datasets
- **Nvidia Stock Data**: Historical stock prices for Nvidia Corporation fetched using the `yfinance` library.
- **Airline Passengers Data**: Monthly totals of international airline passengers from 1949 to 1960.

## 3. Libraries Used
- `pandas`: Data manipulation and analysis.
- `numpy`: Numerical operations.
- `matplotlib`: Data visualization.
- `statsmodels`: Statistical modeling.
- `yfinance`: Fetching financial data.

## 4. Data Loading and Preprocessing
### Nvidia Stock Data
- Data for Nvidia stock prices was downloaded and loaded into a DataFrame. 
- The data was inspected and cleaned for any missing values.

### Airline Passengers Data
- Data for airline passengers was read from a CSV file.
- Missing values were handled and the 'Month' column was converted to datetime format for proper time series analysis.

## 5. Exploratory Data Analysis (EDA)
### Nvidia Stock Data
- **Plotting Open Prices**: The opening prices of Nvidia stocks were plotted to observe the trend over time.
- **Simple Moving Averages (SMA)**: Calculated and plotted to smooth out short-term fluctuations and highlight longer-term trends.
- **Exponential Moving Averages (EMA)**: Calculated and plotted to give more weight to recent prices, thereby capturing more recent trends more effectively.

### Airline Passengers Data
- **Plotting Passengers Data**: The data was plotted to visualize the monthly totals of international airline passengers.
- **ADF Test for Stationarity**: Conducted to check if the time series is stationary. Stationarity is essential for accurate modeling in time series analysis.
- **Differencing for Stationarity**: Applied to make the time series data stationary by removing trends and seasonality.

### Autocorrelation and Partial Autocorrelation
- **Autocorrelation Function (ACF)**: Measures the correlation between the time series and its lagged values. Plotted to identify the extent of correlation with previous time steps.
- **Partial Autocorrelation Function (PACF)**: Measures the correlation between the time series and its lagged values while controlling for the values of the time steps in between. Plotted to identify the direct effect of previous time steps.

## 6. Modeling
### ARIMA Model for Airline Passengers Data
- **Train-Test Split**: The data was divided into training and testing sets to evaluate the performance of the ARIMA model.
- **ARIMA Model Creation and Fitting**: An ARIMA model was fitted to the training data and used to make predictions.

### SARIMA Model for Airline Passengers Data
- **Seasonality Consideration**: The airline passengers data shows clear seasonal patterns. To model this, a Seasonal ARIMA (SARIMA) model was used.
- **SARIMA Model Creation and Fitting**: A SARIMA model was fitted to the training data and used to make predictions. This model incorporates both seasonal and non-seasonal factors in the time series data.

## 7. Definitions of Important Models and Concepts
### Moving Averages (MA)
- **Simple Moving Average (SMA)**: An average of the data points within a certain window. It smooths out short-term fluctuations and highlights longer-term trends or cycles.
- **Exponential Moving Average (EMA)**: A type of moving average that places a greater weight and significance on the most recent data points. This makes it more responsive to recent price changes compared to SMA.

### Stationarity
- A time series is said to be stationary if its statistical properties such as mean, variance, and autocorrelation are all constant over time. Stationarity is important for time series modeling because many statistical methods assume or require a stationary time series.

### Differencing
- A technique used to make a non-stationary time series stationary by subtracting the previous observation from the current observation. It helps remove trends and seasonality from the data.

### Autocorrelation and Partial Autocorrelation
- **Autocorrelation Function (ACF)**: A measure of the correlation between a time series and its lagged values. The ACF plot helps in identifying the extent of correlation with previous time steps and can guide in choosing the appropriate model parameters.
- **Partial Autocorrelation Function (PACF)**: A measure of the correlation between a time series and its lagged values while controlling for the values of the time steps in between. The PACF plot helps in identifying the direct effect of previous time steps and is used to determine the order of the autoregressive part of the model.

### ARIMA Model
- ARIMA (AutoRegressive Integrated Moving Average) is a class of models that explains a given time series based on its own past values (autoregressive part), the differenced values (integrated part), and a moving average model applied to the lagged forecast errors (moving average part).

### SARIMA Model
- SARIMA (Seasonal AutoRegressive Integrated Moving Average) extends the ARIMA model by explicitly modeling seasonal effects. It incorporates seasonal autoregressive (SAR), seasonal differencing (SD), and seasonal moving average (SMA) components along with non-seasonal components. This model is particularly useful for time series data with strong seasonal patterns.

### ADF Test (Augmented Dickey-Fuller Test)
- A statistical test used to determine if a time series is stationary. It tests the null hypothesis that a unit root is present in a time series sample. A lower p-value indicates that the null hypothesis can be rejected, suggesting the time series is stationary.

## 8. Data Visualization
- Visualizations were used extensively to understand data trends and patterns. Examples include:
- Line plots to visualize stock prices over time.
- Comparison of actual vs. predicted values in time series forecasting.

## 9. Model Evaluation Metrics
- To evaluate the performance of the time series models, metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) were used. These metrics help quantify the accuracy of the predictions.

## 10. Hyperparameter Tuning
- For both ARIMA and SARIMA models, parameters such as p (autoregressive order), d (differencing order), q (moving average order), P (seasonal autoregressive order), D (seasonal differencing order), Q (seasonal moving average order), and m (seasonal period) were tuned to achieve the best model fit.

## 11. Conclusion
- This project demonstrated the application of various time series analysis techniques on Nvidia stock data and airline passengers data. Techniques such as moving averages, exponential moving averages, differencing, ARIMA, and SARIMA models were used to analyze and forecast the time series data. The results provide insights into the trends and patterns within the data, which can be useful for making informed decisions in finance and transportation sectors.

## Thank you 😀
