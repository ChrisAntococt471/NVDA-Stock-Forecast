# NVDA-Stock-Forecast
The aim of this notebook is to find the best stock listed in the S&amp;P 500 index to invest in and then predict the said stock's future price with determined models.

S&amp;P 500 Index data is from 2014-07-21 until 2024-07-19 S&amp;P 500 Stocks data is from 2010-01-04 until 2024-07-19

The stock selection is based on weight, as we go for the safest stocks to invest, meaning we go for blue-chip stocks. Based on simple profitability analysis on those stocks, we have chosen NVDA as the best stock to invest in as it has the highest gain during the analysis time frame and also the least variance, which means it has the lowest risk of all.

![NVDA STOCK COMPARISON](https://github.com/ChrisAntococt471/NVDA-Stock-Forecast/blob/main/STOCKS%20GAIN%20COMPARISON.png)

![NVDA STOCK GROWTH](https://github.com/ChrisAntococt471/NVDA-Stock-Forecast/blob/main/NVDA%20ANNUAL%20GROWTH.png)

We used Prophet, Linear Regression, Random Forest Regressor, XGBoost Regressor, and ARIMA models to predict future NVDA stock prices.

In the end, we decided that the ARIMA model is the best fit for the prediciting NVDA price.

![ARIMA](https://github.com/ChrisAntococt471/NVDA-Stock-Forecast/blob/main/ARIMA.png)

![ARIMA](https://github.com/ChrisAntococt471/NVDA-Stock-Forecast/blob/main/Model%20Comparison.png)

Sudden dramatic increase of the NVDA price mostly failed to be anticipated properly by most of the models, especially since the train data only cover up until 2023-10-25, and the dramatic rise of the price still happened after that. So far, only ARIMA, combined with rolling forecast technique can give a better forecast value.

With the data trend like this, some new ideas for the treatment would be:

1. Only using the data from 2023 onwards, since data from previous date looks irrelevant
2. Wait for more data to generate
3. Add new variables for regression predictor (examples like lags, moving average, and others)
