# DS_CapstoneProject_SaudiStockMarket

#### Overview:
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
*Trend: A long-term change in the data is referred to as a trend. 

*Seasonal: When a series is affected by some seasonal factors.
** To remove seasonality from the data, we subtract the seasonal component from the  data..

*Cyclic: When data exhibit rises and falls that are not seasonal

###### Data Cleaning 
* Dividing the data into  the first 7 years of the data going from 2010 - 2017, and leave the last 3 years (2017-2020) to compare the out come. The data will be divided 70/30.


