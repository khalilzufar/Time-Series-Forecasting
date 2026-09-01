# 📈 Tourism Popularity Time-Series Forecasting


A time-series analysis project that forecasts weekly search interest for Pulau Pari using Google Trends data.


## 🎯 Objective


Estimate future tourism popularity from historical weekly search-interest values and compare ARIMA-based forecasting approaches.


## 🗃️ Dataset


The input file multiTimeline.csv contains 126 weekly observations with:


- Week — weekly date.
- Pulau_Pari — Google Trends interest score from 0 to 100.


The notebook uses 101 weeks for training and 25 weeks for evaluation.


## 🔄 Workflow


1. Load and clean the Google Trends export.
2. Parse weekly dates and inspect missing or duplicate observations.
3. Explore the trend, seasonality, stationarity, ACF, and PACF.
4. Train ARIMA and seasonal ARIMA/SARIMAX models.
5. Evaluate the predictions with MAE and MAPE.
6. Generate a 52-week forecast for exploration.


## 📊 Results


| Model | Test MAE | Test MAPE |
| --- | ---: | ---: |
| ARIMA(1,1,1) | 10.24 | 24.30% |
| Seasonal ARIMA/SARIMAX | 11.23 | 29.63% |


On this split, the non-seasonal ARIMA model performed better. The forecast should be treated as directional because the dataset is short and search interest is an external behavioral signal.


## ▶️ Run locally


~~~bash
python -m pip install pandas numpy matplotlib seaborn statsmodels scikit-learn jupyter
jupyter notebook Forecasting.ipynb
~~~


## 👤 Author


[Khalil Zufar](https://github.com/khalilzufar)

