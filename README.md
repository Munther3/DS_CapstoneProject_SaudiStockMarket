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

##### Steps:

1. Exploratory analysis
2. Fit the model
3. Diagnostic measures

The first step in time series data modeling using R is to convert the available data into time series data format using ts() function. 

##### Importnant elements of a time series data 
Trend: A long-term increase or decrease in the data is referred to as a trend. It is not necessarily linear. It is the underlying pattern in the data over time.
Seasonal: When a series is influenced by seasonal factors i.e. quarter of the year, month or days of a week seasonality exists in the series. It is always of a fixed and known period. E.g. – A sudden rise in sales during Christmas, etc.
Cyclic: When data exhibit rises and falls that are not of the fixed period we call it a cyclic pattern. For e.g. – duration of these fluctuations is usually of at least 2 years.

#### Data Cleaning 
* Dividing the data into  the first 7 years of the data going from 2010 - 2017, and leave the last 3 years (2017-2020) to compare the out come. The data will be divided 70/30.

