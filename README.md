# Exploration of Factors Associated with Hate Crime Rates in the US: Project Overview

* **Objective**<br/>
This project aims to build a multiple linear regression model to identify factors that are most closely associated with hate crime rates in the US. With the number of hate crimes jumping at an alarming rate, there is a growing urgency to find trends within the hate crime data that can assist the law enforcement agencies and the FBI to better address and prevent future incidents. 

* **Walkthrough**
    - Define the question and collect the data 
    - Exploratory Data Analysis 
    - Data Cleaning 
    - Fit Multiple Linear Regression Models & Choose Final Model
  
* **Data & Coding Language Used**
    - Data: data of every US state collected from the Southern Poverty Law Center in the first weeks of November 2016 
    - R Version: 4.0.3
    - Packages: tidyverse, arsenal, corrplot, boot

### Exploratory Data Analysis 
* The distribution of each feature was checked.<br/>
  Log transformation was done on the skewed features, which made their distributions more normal.<br/> 
* Using the 1.5 IQR rule, states that might contain outlier outcome values were identified<br/>
  &#8594; the states were Oregon and District of Columbia<br/> 
  &#8594; an extreme outlier value was dropped 
* Correlations between features were checked as well 



### Data Cleaning 
* Data were scaled
* Some variable types were converted to factors 
* Dropped the very few missing values that were present in the dataset 
* Skewed features underwent log transformation

### Fit Multiple Linear Regression Models & Choose Final Model 
* From the correlation matrix, it could be seen that 'median income', 'income inequality', and 'percentage of population with high school degree' are most
  correlated with 'hate crime rate'. Thus, these three independent features were selected for the first multiple linear regression(MLR) model. Each of
  these features are in the unit of a US state.<br/>
  &#8594; The coefficients of 'income inequality' and 'percentage of population with high school degree' had p values lower than 0.05 but the coefficient
  of 'median income' did not<br/>
  &#8594; From the global F-test, it could be concluded that at least one coefficient of the model is not equal to zero<br/>
  &#8594; Adjusted R squared value was checked as well 
  
* Another MLR model was fit without 'median income' this time<br/>
  &#8594; Both the F-statistic and adjusted R squared value increased<br/>
  &#8594; This model was validated using backward elimination, which selected the same features
  
* Lastly, model diagnostics were done<br/>
  &#8594; The histogram of residuals showed a normal distribution<br/> 
  &#8594; The residual plot showed that the residuals do not have a distribution around the line y =0 
  
* Thus, the confirmed final model was:<br/>
  Hate Crime Rate = -3.989 + 3.284 * percentage of HS degree + 3.136 * Income Inequality

