# Multiple_Linear_Regression_Bike_Sharing_Assignment

Problem Statement
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

The company wants to know:
Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands

Methodlogy followed:

1.) Reading data and EDA: 
 Reading data in pandas dataframe 
 Performing Exploratory Data Analysis 
 Visualizing and analyzing of continuous variables using scatter 
plot-pair plots 
 Visualizing and analyzing of continuous variables using box plotsubplots 
 Visualizing and analyzing of continuous variables using heat maps 
2.) Preparing data for modeling: 
 Creating dummy variables for categorical variables 
 Splitting data into test data and train data 
 Rescaling the continuous data using either normalization or 
standardization method 
3.) Training the model: 
 Selection of variables to build the model while building a model is 
a critical aspect 
 If the number of variables is less (around 15) we can use manual 
process for elimination 
 Else we can use RFE to reduce the number of variables to 15 and then 
use manual process to eliminate variables 
 We eliminate variables having p values > 0.05 initially 
 Then we eliminate variables having high VIF> 5 
 We drop variables one by one 
4.) Residual Analysis and evaluation of final model: 
 Errors must be normally distributed about mean 0 
 Check whether error terms are normally distributed with mean about 
zero 
 R2 value indicates the variance of the model we can check whether 
the model is overfitting (around 80% is desiarable) 
 P(F Statistic) indicates whether model fit is significant 
 P value < 0.05 indicates significance of model 
 We can compare actual values with predicted values on training data 
 We can check VIF of variables for multicolinearity; VIF>5 indicates 
colinearity among variables 
5.) Predications and evaluations on test set 
 Rescale the data for test variables 
 Predict values for test data using final model 
 Compare predicted values and actual values using scatter plot; look 
for an approximate linear relationship 
 Find out the R squared value between test and predicted test data 
sets it must be close to the models R2 
 Plot the error terms - there should not be any specific pattern 


Outcome: The final model derived is as follows:
 OLS Regression Results                            
==============================================================================
Dep. Variable:                    cnt   R-squared:                       0.836
Model:                            OLS   Adj. R-squared:                  0.832
Method:                 Least Squares   F-statistic:                     230.3
Date:                Thu, 29 Jul 2021   Prob (F-statistic):          2.65e-187
Time:                        19:37:31   Log-Likelihood:                -4126.3
No. Observations:                 510   AIC:                             8277.
Df Residuals:                     498   BIC:                             8327.
Df Model:                          11                                         
Covariance Type:            nonrobust                                         
==============================================================================================
                                 coef    std err          t      P>|t|      [0.025      0.975]
----------------------------------------------------------------------------------------------
const                       1369.5213    169.677      8.071      0.000    1036.150    1702.893
yr                          2029.3168     71.455     28.400      0.000    1888.927    2169.707
holiday                     -831.6702    226.371     -3.674      0.000   -1276.430    -386.910
temp                        4268.5169    213.127     20.028      0.000    3849.777    4687.257
windspeed                  -1365.0121    219.342     -6.223      0.000   -1795.962    -934.063
season_Summer                817.6965     99.579      8.212      0.000     622.050    1013.343
season_Winter               1095.8294    100.822     10.869      0.000     897.741    1293.918
mnth_Aug                     451.9665    144.371      3.131      0.002     168.315     735.618
mnth_Jan                    -366.9511    154.974     -2.368      0.018    -671.434     -62.468
mnth_Sept                    987.8871    143.124      6.902      0.000     706.686    1269.088
weathersit_Light Rain/Snow -2463.6061    214.729    -11.473      0.000   -2885.492   -2041.721
weathersit_Mist             -696.5515     76.393     -9.118      0.000    -846.644    -546.459
==============================================================================
Omnibus:                       56.180   Durbin-Watson:                   2.067
Prob(Omnibus):                  0.000   Jarque-Bera (JB):              121.643
Skew:                          -0.614   Prob(JB):                     3.85e-27
Kurtosis:                       5.053   Cond. No.                         11.8
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
                      Features   VIF
2                         temp  5.05
3                    windspeed  3.34
0                           yr  2.04
4                season_Summer  1.89
6                     mnth_Aug  1.59
5                season_Winter  1.55
10             weathersit_Mist  1.54
8                    mnth_Sept  1.31
7                     mnth_Jan  1.22
9   weathersit_Light Rain/Snow  1.08
1                      holiday  1.04

Test Model Performance:
![image](https://user-images.githubusercontent.com/96782623/147845929-a582dc4b-7fae-4119-8e7f-6d3ded7b64a5.png)
