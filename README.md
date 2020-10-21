# IBM DS Capstone Project

## Introduction
This repository holds the notebook files for the capstone project that is part of my IBM Data Science Professional Certificate. Keep in mind that this is the first project I have ever done in the field of data science and I am still quite new so it won't be perfect however, any feedback is greatly appreciated. Also as this is a repo based on the course's requirements, some aspects of a normal data science project may be absent in this repo or incomplete altogether.

## What I learnt:
- Basic git commands
- Basic analytical and statistical methods
- Using pandas to import and save csv files
- Using pandas to explore and manipulate data
- Basic data visualisation with matplotlib, seaborn
- Creating choropleth map with folium
- Find correlation using scipy
- Visualising correlation using correlation matrix
- Prepare data for model building
- Create and train logistic regression, multiple linear regression, and K-nearest neighbours models
- Evaluate models for their accuracy

## Feedback I recieved on the Analysis and Report:
- Remember the whole purpose of the analysis and what information am I trying to find. How can my findings and predictive model be useful to clients? For example, can I use the findings to urge building owners to review their buildings? Write a conclusion to the report and link it to the overall problem I am trying to solve.
- Making a boxplot for the number of complaints would have helped visualised the variance of the data which could have guided me in a direction to take for model building such as creating models to predict if a building will land in the top certain percentage of complaints made.
- Try to keep the dataset for the model varied to prevent overly unbalanced data. It was highly likely that because the predictive model’s training data solely consisted of buildings in the Bronx, the data was unbalanced as a result of the already large proportion of buildings that received complaints compared to ones that did not. Instead, I should have included more geographical locations in the model building stage.
- Do not worry about extremely low p-values especially because they had extremely low Pearson correlations and my dataset was very large. Also, if features have extremely low Pearson correlations, then I should not have used them as features in the model. Overall, I needed to analyse the Pearsons and p-value more closely before creating any models.
- I did not report on the models clearly and there were parts that were not necessary such as the models’ data sections. Regarding the multiple linear regression, it is important to state the coefficients and intercept with an epsilon as an equation. 
- Potentially look at Cohen’s kappa, ROC curves, stepwise multiple linear regressions, variance inflation factor linear models, residual plots, and decision trees for regression.

## Included Files:
- Question 1.ipynb (Clean main dataset and light exploration to find what problem the department should focus on first)
- Question 2.ipynb (Found out the amount of heating complaints depending on the location of the house)
- Question 3.ipynb (Found correlation between housing characteristics and whether a complaint has/will be made)
- Question 4.ipynb (Created and evaluated machine learning models for the heating complaints)
- Final Report.ipynb (This is the notebook that I created the report in)
- Final Report.html (Report)

## Problem Statement
The people of New Yorker use the 311 system to report complaints about the non-emergency problems to local authorities. Various agencies in New York are assigned these problems. The Department of Housing Preservation and Development of New York City is the agency that processes 311 complaints that are related to housing and buildings.

In the last few years, the number of 311 complaints coming to the Department of Housing Preservation and Development has increased significantly. Although these complaints are not necessarily urgent, the large volume of complaints and the sudden increase is impacting the overall efficiency of operations of the agency.

Therefore, the Department of Housing Preservation and Development has approached your organization to help them manage the large volume of 311 complaints they are receiving every year.

The agency needs answers to several questions. The answers to those questions must be supported by data and analytics. These are their  questions:

1. Which type of complaint should the Department of Housing Preservation and Development of New York City focus on first?
2. Should the Department of Housing Preservation and Development of New York City focus on any particular set of boroughs, ZIP codes, or street (where the complaints are severe) for the specific type of complaints you identified in response to Question 1?
3. Does the Complaint Type that you identified in response to question 1 have an obvious relationship with any particular characteristic or characteristics of the houses or buildings?
4. Can a predictive model be built for a future prediction of the possibility of complaints of the type that you have identified in response to question 1?

Your organization has assigned you as the lead data scientist to provide the answers to these questions. You need to work on getting answers to them in this Capstone Project by following the standard approach of data science and machine learning.

## Resources and Datasets Used

**Python Version:** 3.8

**Packages:** pandas, numpy, scipy, sklearn, matplotlib, seaborn, folium, itertools

I have used two datasets that the course provided in this project and also one geographical json file.

#### 311 complaint dataset

The dataset I used was already placed on an IBM server which is where I got it from. You can download the data using this link: https://cocl.us/311_NYC_Dataset. The downloaded data will have complaints submitted between 2010 and 2020.
The original dataset is available at https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9. You can download part of this data by using SODA API.

#### PLUTO dataset for housing

The dataset I downloaded comes from here: https://www1.nyc.gov/assets/planning/download/zip/data-maps/open-data/nyc_pluto_18v1.zip. This comes in a zip file which will need to be extracted first before the data can be used.
The original dataset for housing can be accessed from https://data.cityofnewyork.us/City-Government/Primary-Land-Use-Tax-Lot-Output-PLUTO-/xuk2-nczf. 


#### Data on borough boundaries in New York

This contained geographical data about the boundaries of the boroughs in New York in a geojson format. This was use in the question 2 notebook to help with the analysis of the geographical effects on the number of complaints made. This data can be accessed from https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm. The data does not need to be downloaded as the code in the notebook already downloads it automatically when run.
