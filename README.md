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

