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

After the completion of first iteration, the following results were obtained:
![image](https://github.com/Shimnazzz/dsc-phase-2-project/assets/147800579/85293e70-9739-4780-9637-ce33fa024736)

The adjusted R square value was found to be 0.562 which means that 56% of variance of price can be explained by this model. and the model has high significance. In terms of the significance of the features, all features except sqft_lot was found to be siginificant to explain the dependant variable. 

To confirm the linear regression assumptions, the Q-Q plot was plotted as shown below: 
![image](https://github.com/Shimnazzz/dsc-phase-2-project/assets/147800579/9604989b-ced4-49f5-91f4-cd2ad7f24337)

The residuals, from the above plot can be seen that are not completely normal and some skewness is present. Also from the fitted values vs residuals plots for each varaibles, conical shape was seen in the case for sqft_lot, sqft_lot15 as shown below
![image](https://github.com/Shimnazzz/dsc-phase-2-project/assets/147800579/84315376-6a15-4158-b121-a6372ddd8378)

After the doing iteration 2, these two variables were part of the variables removed for multicollinearity and therefore impact on the assumptions of linear regression model can be avoided.

After completion of Iteration 4, the following result was obtained after running the statsmodel:
![image](https://github.com/Shimnazzz/dsc-phase-2-project/assets/147800579/2d2825ff-6522-4704-89b8-b1790c78bc8d)

The adjusted R square was observed to be 0.530, which is a clear reduction from the first iteration. Even though the percentage of variance of the price explained by the model has reduced, the assumptions of linear regression has become more valid in this model. This is clearly seen in the JB value reducing from 217 to 68. This can also be seen in the straightness of the datapoints in the Q-Q plot of this model below:

![image](https://github.com/Shimnazzz/dsc-phase-2-project/assets/147800579/979e53fe-4f1a-451c-a736-8c99241347a8)

The model was also validated by checking the measn sqaure error of the training and test data set. The value for the former was 0.103365 while the latter value was 0.103383. Since the mean square error for the testing data set was slightly higher but within the close range of that of training data set, we can confirm that the model is not overfitting but slightly underfitting.

### Inferences

* Based on the coefficients, the features with high impact on price are sqft_living, floors, waterfront view, condition, grade and renovations.
* The recommendations can be derived for King COunty Real Estate Agent for targetting the high price properties:
    * The number of floors can have a positive impact on the price. The log of price will increase by 0.23 - 0.578 by having 2 - 3 floors. In other words there will an increase in price by 1.26 - 1.78 times the value of the property.
    * Having a waterfront property can improve the price by 1.4 times the value of the property.
    * Better the condition and grade (in terms of the Kings County Grading system), better will be the price of the property. Improved condition of the propoerty can increase the value of the property by 1.4 - 1.85 times the value of the property. Having a grade of 11 can imcreae the price of the property by 9 times.

* The real estate agency could provide the following recommendations to potential sellers to improve the value of the property:
    * Doing a renovation can increase the value of the house by around 1.25 times the value of the house.
    * Properties with just one bathroom depreciated the value of the house by 0.91 times. therefore, increasing the number of bathrooms while doing the renovations would be recommended.
