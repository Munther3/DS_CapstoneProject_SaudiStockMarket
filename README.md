# DS_CapstoneProject_SaudiStockMarket

# Overview:
* For this project I will start with a general idea of the market price, including dataset analysis. Followed by a general description and analysis of the dataset. The objective is to apply different forecasting predictive models for the Saudi stock market daily close price. The models will be evaluated, analysed and compared, following the main course project directions. For this evaluations I will focus in the train set accuracy performance of the models, trying to simplify our analysis due to our aim is showing new forecasting applications and encourage the open source use of them. 

* This report describes different time series and machine learning forecasting models applied to a Sadui stock market (Tadawuel) close price for he past 10 years, up untill the the end of last month data.  The data will be divided 70/30. I will divie into analyzing the first 7 years of the data going from 2010 - 2017, and leave the last 3 years (2017-2020) to compare the out come.

## Models 

### ARIMA 

* ARIMA is the abbreviation for AutoRegressive Integrated Moving Average. Auto Regressive (AR) terms refer to the lags of the differenced series, Moving Average (MA) terms refer to the lags of errors and I is the number of difference used to make the time series stationary.

#### Assumptions of ARIMA model

1. Data should be stationary 
2. Data should be univariate 
##### To achieve stationarity:
* Difference the data by computing the differences between consecutive observations
#### Steps:

1. Exploratory analysis
2. Fit the model
3. Comparing the model with test data 
##### EDA:
The first step in time series data modeling using R is to convert the available data into time series data format using ts() function. 

###### Importnant elements of a time series data 
1. Trend: A long-term change in the data is referred to as a trend. 

2. Seasonal: When a series is affected by some seasonal factors.
(to remove seasonality from the data, we subtract the seasonal component from the  data)

3. Cyclic: When data exhibit rises and falls that are not seasonal

###### Data Cleaning 
* Dividing the data into  the first 7 years of the data going from 2010 - 2017, and leave the last 3 years (2017-2020) to compare the out come. The data will be divided 70/30.
##### Fitting auto.arima model 

1. To better find the values of p,d,q we use the function auto.arima()

2. The auto.arima() function in R uses a combination of unit root tests, minimization of the AIC and MLE to obtain an ARIMA model.

3. What is AIC? Akaike's Information Criterion (AIC), which was useful in selecting predictors for regression, is also useful for determining the order of an ARIMA model.

4. The p,d, and q are then chosen by least value of AIC.  

##### Comparasion
1.I focus on forecasting the close stock price for the next 3 years so that I can compare the outcome with the test data, which has the data for the targeted period by the model

2. This is the overall process by which we can analyze time series data and forecast values from existing series using ARIMA.

### Prophet model

1. The origin of prophet comes from the application of a forecasting model into supply chain management, sales and economics. This model helps with a statistical approach in shaping business decisions.The Prophet model has been developed by Facebook’s Core Data Science team and it is an open-source tool for business forecasting.

2. The Prophet model is an additive model with the components g(t) models trends, s(t) models seasonality with Fourier series, h(t) effects of holidays or large events.

#### Steps 

##### Conversion
The fist step before forecasting using prophet is to convert the dataset into the format that Prophet input requires.

#####
With the model applied and the forecast plotted we proceed to calculate the model performance

### Feed Foward Neural network
1. Researching deeply in new machine learning models I have reached some new neural network function in the forecast package called nneta

2. A single hidden layer neural network is the most simple neural networks form. In this single hidden layer form there is only one layer of input nodes that send weighted inputs to a subsequent layer of receiving nodes. This nnetar function in the forecast package fits a single hidden layer neural network model to a timeseries. The function model approach is to use lagged values of the time series as input data, reaching to a non-linear autoregressive model.

## Comclusion 

* In this project I focus in the application of different models, learning how to use them with the objective to forecast new price values. As we will see from the results, the models performed with similar future tendency predictions. All the models predicted a tendency of a lower price in next 3 years. We will conclude that the ARIMA and prophet performed very well inside the prediction intervals and the accuracy metrics. The Neural Net models model did not performed as well as ARIMA or prophet models. Maybe it needed more tuning for getting more accurated results.
