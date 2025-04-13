# Time Series Forecasting Using the Decomposition Technique

*Tools Used: Python (Jupiter Notebook)*

## Introduction
This report presents an analysis of airline passenger data using time series decomposition techniques. The dataset includes monthly records of airline passengers in the United States from 1949 to 1960. The objective of this study is to examine historical trends and seasonality to forecast passenger numbers for the final year (1960) and assess forecasting accuracy.

## Methodology
The time series decomposition method was employed to analyze the data. This process involved the following key steps:

1. **Data Preparation:**
   - The dataset includes monthly passenger counts for 12 years (1949-1960).
   - The last year (1960) was set aside for validation purposes.

![image](https://github.com/user-attachments/assets/2fa9ea97-9702-40f9-97a1-c05f691f2c70)

2. **Moving Average Calculation:**
   - A 16-month moving average was computed to extract the trend component by smoothing out short-term fluctuations.

![image](https://github.com/user-attachments/assets/c621efb4-caa5-4f1d-bf95-c83bb8fd8b0c)

3. **Seasonal Factor Calculation:**
   - The seasonal indices were determined by dividing actual values by the corresponding moving average values.
   - The average of these indices over multiple years provided a reliable seasonal pattern.

4. **Deseasonalization and Trend Projection:**
   - The raw data was deseasonalized by dividing the original values by seasonal factors.
   - A regression model was fitted to the deseasonalized data to estimate the trend.
   
5. **Forecasting for 1960:**
   - Using the derived trend equation, the passenger numbers for each month in 1960 were forecasted.
   - The final forecasts were obtained by multiplying trend estimates by seasonal factors.

![image](https://github.com/user-attachments/assets/3b379c6b-37e1-43f3-aeeb-2386d8f20a44)

![image](https://github.com/user-attachments/assets/4b5d7eb4-04da-40bf-a501-25f4f5641b69)

6. **Error Calculation:**
   - The forecasting error was assessed by comparing predicted values with actual values from 1960.
   - Key error metrics such as Mean Absolute Error (MAE) were calculated to evaluate model performance.

![image](https://github.com/user-attachments/assets/a5179510-ab23-4ad0-9d65-033f4cb22528)


## Results and Interpretation
### Trend Analysis
The moving average approach revealed an upward trend in airline passenger numbers over the 11-year period. A steady increase in passengers suggests consistent growth in air travel demand during this period.

### Seasonal Pattern
The seasonal indices indicated recurring monthly fluctuations, with peaks typically occurring in the summer months (June, July, and August) and lower passenger counts in winter months (January and February). This pattern aligns with expected vacation and holiday travel trends.

### Forecasting Accuracy
The comparison between predicted and actual values for 1960 revealed minor deviations. The MAE was calculated to assess the accuracy of the forecast, with a relatively low error margin indicating a robust forecasting model.

## Conclusion
This study demonstrates the effectiveness of time series decomposition in forecasting airline passenger numbers. The results highlight a clear trend and strong seasonal effects, allowing for accurate predictions. The methodology applied can be extended to similar time series forecasting tasks in business analytics, aiding in demand planning and strategic decision-making.


