### Time Series EDA and Stock Analysis of Tesla (2010-2024)

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
