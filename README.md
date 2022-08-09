# Exploration of Factors Associated with Hate Crime Rates in the US: Project Overview

* **Objective**<br/>
This project aims to build a multiple linear regression model to identify factors that are most closely associated with hate crime rates in the US. With the number of hate crimes jumping at an alarming rate, there is a growing urgency to find trends within the hate crime data that can assist the law enforcement agencies and the FBI to better address and prevent prevent future incidents. 

* **Walkthrough**
    - Define the question and collect the data 
    - Exploratory Data Analysis 
    - Data Cleaning 
    - Fit Multiple Linear Regression Models & Choose Final Model
    - Interpretation
  
* **Data & Coding Language Used**
    - Data: data of every US state collected from the Southern Poverty Law Center in the first weeks of November 2016 
    - R Version: 4.0.3
    - Packages: tidyverse, arsenal, corrplot, boot

### Exploratory Data Analysis 
* The distribution of each feature was checked.<br/>
  Log transformation was done on the skewed features, which made their distributions more normal.<br/> 
* Using the 1.5 IQR rule, identified states that might contain outlier outcome values<br/>
  &#8594; the states were Oregon and District of Columbia 

### Data Cleaning 
* Dropped the very few missing values that were present in the dataset 
* Data were scaled 
* Skewed features underwent log transformation
* Some variable types were converted to factors 

### Fit Multiple Linear Regression Models & Choose Final Model 


### Interpretation 
