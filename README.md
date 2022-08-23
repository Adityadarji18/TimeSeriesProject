# TimeSeriesProject

Problem Statement -
Forecast future sales using historic sales data.

Solution -
1) Checked the sales plot the data is seasonal ie. there are trends after every specific interval of time.
2) Checked for stationarity of the data using Dickey-Fuller test , the p val was 0.36 ie. we reject the null hypothesis and hence we can say that the data is non stationary
3) Now to fix this I used differencing technique were I differenced the data by 12 since it is a seasonal data , after which the pval < 0.05 and hence the data is stationary.
4) Then I have used the SARIMA model (Seasonal Autoregressive Integrated Moving Average) to forcast the future values.
Specifically the model, SARIMA means some response variable (Y) by combining a 1st order Auto-Regressive model and a 1th order Moving Average model with once of time the data is differenced.
Here in pacf and acf at lag 1 the values is just close to the critical range and hence we can consider p and q to be 0 or 1
and we differenced the data once hence d will we 1 and in seasonal_order the seasonal difference will be by 12.

![image](https://user-images.githubusercontent.com/67514632/186091209-59440e9f-3fa4-4d2b-8811-afbbebf7bd78.png)
