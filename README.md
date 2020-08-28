# Studentized OLS Classifier
> This is a custom classifier created using Scikit Learn's project template for custom estimators.
> This project was inspired by the Enron email dataset where I used a typical studentized OLS process to check for outliers
> but I was suprised to find that 16 of 17 outliers found were people of interest and this method correctly identified 16 of 19 POI's.  
> The model uses statsmodels OLS for the initial fit. Predict then uses the same OLS model to make a 
> prediction. The median of the predictions is subtracted from the prediction to create an estimated 
> residual. The estimated residual is then divided by the standard deviation of the residuals from the fit
> to create an estimated studentized residual. These studentized residuals are then tested against the
> hyperparameter "threshold" to determine the label. All  values greater than or equal to the threshold are 
> labeled True, and values less than the threshold are labeled False.
