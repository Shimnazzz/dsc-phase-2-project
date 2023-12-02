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

Since the prime focus accessing the factors affectin the price of the property, the dependable variable is considered as "price" for the analysis. Also assuming that the latitude, longtiude and zipcode will not have a linear relationship with the price and hence these three parameters will not be used in the analysis. Eventhough location of property has high significance on the price of the property, it need not have a linear correlation with the price. In simpler words, we could not say that with the increase in the latitude values, the price of teh proporty will increae or decrease. Hence these parameters were dropped in the beginning of teh analysis itself.


## Deliverables

There are three deliverables for this project:

* A **GitHub repository**
* A **Jupyter Notebook**
* A **non-technical presentation**

Review the "Project Submission & Review" page in the "Milestones Instructions" topic for instructions on creating and submitting your deliverables. Refer to the rubric associated with this assignment for specifications describing high-quality deliverables.

### Key Points

* **Your deliverables should explicitly address each step of the data science process.** Refer to [the Data Science Process lesson](https://github.com/learn-co-curriculum/dsc-data-science-processes) from Topic 19 for more information about process models you can use.

* **Your Jupyter Notebook should demonstrate an iterative approach to modeling.** This means that you begin with a basic model, evaluate it, and then provide justification for and proceed to a new model. After you finish refining your models, you should provide 1-3 paragraphs discussing your final model - this should include interpreting at least 3 important parameter estimates or statistics.

* **Based on the results of your models, your notebook and presentation should discuss at least two features that have strong relationships with housing prices.**

## Getting Started

Start on this project by forking and cloning [this project repository](https://github.com/learn-co-curriculum/dsc-phase-2-project) to get a local copy of the dataset.

We recommend structuring your project repository similar to the structure in [the Phase 1 Project Template](https://github.com/learn-co-curriculum/dsc-project-template). You can do this either by creating a new fork of that repository to work in or by building a new repository from scratch that mimics that structure.

## Project Submission and Review

Review the "Project Submission & Review" page in the "Milestones Instructions" topic to learn how to submit your project and how it will be reviewed. Your project must pass review for you to progress to the next Phase.

## Summary

This project will give you a valuable opportunity to develop your data science skills using real-world data. The end-of-phase projects are a critical part of the program because they give you a chance to bring together all the skills you've learned, apply them to realistic projects for a business stakeholder, practice communication skills, and get feedback to help you improve. You've got this!
