# ARIMA Model for Stock Price Forecasting
This ARIMA model possesses exceptional capabilities in accurately predicting stock prices. Initially, it collects data from Yahoo Finance within a specified timeframe. The data is then decomposed to isolate the trend component, which is utilized for comparing stocks among themselves. Fast Dynamic Time Warping (FastDTW) and Granger Causality techniques are employed to assess the similarity between each stock and the S&P500 index. The Dickey-Fuller test is applied to determine if the model exhibits stationarity. Subsequently, a function is created to compare the trend of two stocks using Dynamic Time Warping (DTW) with Euclidean distance over a selectable date range. An autoregressive model (p, q, d) is generated to forecast future behavior, with the values of p, q, and d determined by visualizing the autoregressive charts and using the AIC criterion.

The data is gathered from Yahoo Finance.

## FastDTW
It is a computationally efficient algorithm used for measuring the similarity between two time series or sequences. It is specifically designed to address the time and space complexity issues associated with the traditional Dynamic Time Warping (DTW) algorithm. By approximating the optimal alignment between two sequences, FastDTW enables faster processing and reduces the computational burden while maintaining a reasonable level of accuracy. It is commonly employed in various fields, including pattern recognition, speech recognition, and data mining, to compare and analyze time-based data efficiently.

## Granger Causality
Granger Causality, in short, is a statistical concept used to determine if one time series can be considered as a predictor of another time series. It explores the cause-and-effect relationship between two variables by analyzing their historical patterns and statistical properties. If one variable's past values provide valuable information for predicting the future values of another variable, it is said to have Granger-causal influence over the latter. Granger Causality helps in understanding the temporal dependencies and interactions between variables, particularly in fields such as econometrics, finance, and social sciences

## Dicky Fuller Test
It is a statistical test used to determine if a time series possesses a unit root, indicating non-stationarity. It examines whether the data exhibits a trend, making it unsuitable for certain statistical analyses that assume stationarity. The test compares the autoregressive relationship of the series with the null hypothesis of a unit root presence. If the test rejects the null hypothesis, it suggests that the series is stationary, implying that it does not exhibit a trend and is suitable for further analysis using stationary models. The Dickey-Fuller test is widely used in econometrics and time series analysis to assess the stationarity of data.

## for Akaike Information Criterion (AIC)
It is a measure used in autoregressive models to assess the quality of fit while considering the model's complexity. It balances the trade-off between model accuracy and simplicity. AIC takes into account both the goodness of fit of the model and the number of parameters used. The lower the AIC value, the better the model is considered. It helps in comparing different autoregressive models and selecting the one that provides the best balance between accuracy and simplicity. AIC is a widely used criterion in statistical modeling and helps in model selection and evaluation.
