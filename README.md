# Time-Series-stock-value-prediction-1
This is the first approach to use time series to predict stock prices.
The objective of this work is to generate a model that allows predicting the price of a financial asset / cryptocurrency in a general way, providing few inputs and giving as output information of different models and which one is the best predictor.

In this model I will create a function that uses the next inputs:
- stock symbol
- the day to start predictions
- Frequency desidered (can be daily or monthly)

This function will do the next steps (explained depply in the code):
1) Gather data from Yahoo Finance API. Depending on the choosen interval, it will collect different amount of past periods.
2) Model the stationary components for months and weekdays, by decomposing the dates in dummies variables. Clean monthly data to have just one observation per month.
3) Decompose the components of the time series (Trend, Seasonality, Residuals, Cycles) and graph historical data of the stock, gathered in point 1.
4) Divide the train and the test data depending on the interval.
5) Create 6 different models (linear - quadratic - logaritmic with and without seasonality), calculate if their series are stational or not and callect all their data in a new dataframe.
6) Make ARIMA models, with the stationary models of point 5, tunning their variables (p,d,q), calculating the RMSE (root mean squared error) for each model and choosing the best one for each.
7) Later, we show a DataFrame which show all models ordered by RMSE value. We can tell that the best model will be the one that has the minimum RMSE.
8) Ending with the analysis we can graph the predicted data for train and test values on each model.


Next steps:

- Use this first model as a base for predicting several stocks quotes at the same time and recommend the best in which to invest some money. In the other hand, recommend if you have to take out your money from some stock.
- Use this model to make a kind of inversion bot to buy, hold, or sell each day.


Special Thanks to my teammates!
