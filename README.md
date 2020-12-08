# Unit 10: Time Series
#### Columbia University • Fu Foundation School of Engineering & Applied Science
##### Contributor:  Lisa Esberger
##### Published:  December 3, 2020

## Linear Regression Forecasting

*Does this model perform better or worse on out-of-sample data compared to in-sample data?*

  *In-Sample Root Mean Squared Error (RMSE): 0.596204*
  *	Training Set: Estimation and model selection
  
  *Out-of-Sample Root Mean Squared Error (RMSE): 0.415454*
  *	Testing Set: Evaluates forecasting performance 

  The in-sample RMSE is higher than the out-of-sample RMSE, so this indicates underfitting is likely.  In this case, the out-of-sample RMSE is “better.”

  Underfitting is appropriate for making decisions where a reasonable excess of false positives would not be of great detriment such as when deciding which households would be likely to be enticed by Bed, Bath & Beyond coupons.  

  However, making decisions based on models where significant underfitting is present would be highly inappropriate in health care cases, for instance recommending a patient begin chemotherapy for a cancer false positive would be detrimental to their health.

  With this particular case involving predictions around Yen Futures, more information would be needed to determine if this model is sufficient for the decisions that are to be made around their purchase, sale or the timing around international trade.

## Time Series Forecasting

*Initial Assumptions*

The starter file indicates that the data reflects USD/Yen in one place and Yen/ USD in another, so in order to determine whether an increase or decrease in the price would be positive or negative, I looked up the average price of USD to Yen in 1976, 1992, 2011 and 2019.

* 1976: 1 USD would buy 295 Yen
* 1992: 1 USD would buy 128 Yen
* 2011: 1 USD would buy 80 Yen
* 2019: 1 USD would buy 109 Yen

From 1976 to 2019, the dollar has weakened relative to the yen.  Also, since the prices noted in the CSV file increase from 1992 to 2011 and decrease from 2011 to 2019, an increase of price would indicate that $1 (USD) buys less yen, therefore, for someone looking to convert their USD to yen, an increase in price would be disadvantageous, and a decrease in price would be advantageous.  This is also reflected on the yen_trend plot generated through the Hodrick-Prescott Filter.

*Based on your time series analysis, would you buy the yen now?*

When the price increases, the same dollar would buy less yen.  The ARIMA model indicates an expected increase in price, therefore we are expecting $1 (USD) to buy more Yen today (10/15/2019) then at any point within the next 5 days.  If we are needing yen later this week, we should buy yen today. 

*Is the risk of the yen expected to increase or decrease?*

The risk of the yen is expected to increase slightly over the next 5 days, however, the beta is slightly less than 1.

*Based on the model evaluation, would you feel confident in using these models for trading?*

R-squared = 0% which indicates that the model explains none of the variability of the response data around its mean.  Since the past price is not indicative of the variation in the future price, I do not believe predicting the future with accuracy is likely.  I would not feel confident using these models for futures trading.
