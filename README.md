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
![Untitled](https://user-images.githubusercontent.com/96782623/147845996-cb4bfbc3-51be-4bde-a6d9-0d84fe932a37.png)

 
Test Model Performance:
![image](https://user-images.githubusercontent.com/96782623/147845929-a582dc4b-7fae-4119-8e7f-6d3ded7b64a5.png)
