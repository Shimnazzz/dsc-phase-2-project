# Phase 2 Project
Welcome to the Repository for Project 2 created by Shimnaz Fathima! You will find a brief overview of the project, the findings and the recommendations derived after the completion of this project here. Please feel free to browse through the files to know more about the iterations and regression models developed in this project.

## Project Overview

This project involves using the data of housing sales in the Northwestern county of King County and recommending the client, King County Real Estate, a real estate agent in the region on aspects related to houses that will improve the value of the property. 

### Business Problem

This project uses Multilinear Correlation theory to assess the features that improve the price of the property and recommend it to our client King County Real Estate. These recommendations will used by them to target houses with high value and also to recommend their potential house selling clients on increasing their value of the property. After the analysis, the factor by which the value of the property will increase for each feature will be discussed.

### The Data

This project uses the King County House Sales dataset which includes the price of the property and related parameters which is listed below with the corresponding column names in the dataset:

* No of berdrooms (bedrooms)
* No of bathrooms (bathroom)
* Sqft footage of the home (sqft_living)
* Sqft footage of the lot (sqft_lot)
* No of floors in the house (floors)
* If the house has a view to a waterfront (waterfront)
* Number of views made by customer (view)
* Overall condition of the house (condition)
* Overall grade given to the husing unit based on King County grading system (grade)
* Sqft footage of the house apart from the basement (sqft_above)
* Sqft footage of the basement (sqft_basement)
* Year the house was built (yr_built)
* Year when house was renovated (yr_renovated)
* Zipcode (zipcode)
* Latitude of the house location (lat)
* Longitude of the house location (long)
* The square footage of interior housing living space for the nearest 15 neighbours (sqft_living15) 
* The square footage of the land lots of the nearest 15 neighbors (sqft_lot15)

### Methodology

Since the prime focus accessing the factors affectin the price of the property, the dependable variable is considered as "price" for the analysis. Also assuming that the latitude, longtiude and zipcode will not have a linear relationship with the price and hence these three parameters will not be used in the analysis. Eventhough location of property has high significance on the price of the property, it need not have a linear correlation with the price. In simpler words, we could not say that with the increase in the latitude values, the price of the property will increase or decrease. Hence these parameters were dropped in the beginning of the analysis itself.

The project then progresses through four iterations. They are described as below:

#### Iteration 1:
In this iteration, a general understanding of the data is obtained through plotting histograms and scatter plots. Based on this required corrections were made such as removing 0 values from sqft_basement which was making the data highly skewed. After that the statemodel was run and relevant statistical parameters like Adjacent R- square value, model significance, significance of different predictors, the skewness and Kurtosis of the model were determined. Also by plotting the Q-Q plot and the Fitted value Vs the Residuals plot for checking the normality of model residuals and the Heteroscedasticity/Homoscedasticity assumption.

#### Iteration 2:

In order to improve the model, multicollinearity among the variables were checked and variables with correlation factor greater than 0.75 was considered as highly correlated and n-1 variables were removed, where n denotes the number of variables with high correlation among each other. Also dummy variables were introduced for the categoracal variables and to avoid dummy variable trap, one of the column in each dummy variable set was removed.

After this the statsmodel was run and the relevant statistical measures were recorded.

#### Iteration 3:

In this iteration, to remove the skewness of the conitnuous variables, log transformation was performed and to bring the values to a uniform scale, feature scaling was performed. Further to this statsmodel was run and if here is any improvement in the model was checked.

#### Iteration 4:

After the previous iteration, stepwise forward and backward regression was performed to understand the which features are highly significant and with low significance in the model. Statsmodel was run again after removing the least significant features in the model. The improvement in the results were recorded and inferences for the client was derived from this model.

#### Model Validation:

After the 4th iteration, model validation was performed by splitting the data into training and test dataets. Log tranformation was done on the conitnuous variables and One Hot Encoding was performed on the categorical variables to convert them to numerical values. The mean square error between the estimated output and actual output was determined for both the training and test datasets. Based on this result, the model was evaluated to be over-fitting or under-fitting.

### Results

