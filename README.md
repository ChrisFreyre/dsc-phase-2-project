# Phase 2 Project

<h1 align=center>King County Housing Analysis</h1>

![graph1](./Images/house_sale1.png)
![graph1](./Images/house_sale1.png)
![graph1](./Images/house_sale1.png)
![graph1](./Images/house_sale1.png)

**Author: Chris Freyre**



## Project Overview & Business Problem

In this project I will provide information, using regression modeling analysis of house sales data in King County, for Real-State agencies to advise home owners on how performing a renovation might increase price of home sales and if so, what factors are relevant to this renovation.


### Data Understanding

From kc_house_data.csv. the data contains a record of 21597 houses sold in the King County in the period of 2014-2015. We have what it seems 9 categories within the data. First we have id and date which do not appear to be relevant at this stage, next we have price prediction target which will be our dependant variable. Thirdly we have quantity of bedrooms, bathrooms and floors, there is also a scored system for the properties by grade and condition. We also have several dimensions in square foot such as living area, lot area, above and basement, we will investigate in depth for the most relevant. We have location data by zipcode, lat, long and square foot 15 (nearest 15 neighbours). Lastly we have year built, year renovated, views and waterfront.

Also proced to investigate unique values in columns:

* Waterfront
* Views
* Grade
* Condition

![graph1](./Images/data_info.png)
Through viewing the initial data, I can see the data types we are working with, they are: integers, floats and objects - it is clear that we'll need to investigate and clean the data.
![graph1](./Images/histogram1.png)

## Data Cleaning

* I started checking for duplicates using "ID" column, where I proceeded to delete the duplicates. 
* Noticed that in "Sqft_living" column we had it as an object data type, this lead me to find and replace "?" for "0"
* "Yr_renovated" column was a data type float so I changed it to integer.
* Checking for missing values, there were only located in "waterfront", "view" and "yr_renovated" columns.

After having cleaner data and a much better undestanding of it, I proceeded to drop columns not related to the task. Dropping ID, date, view, sqft_above, sqft_basement, yr_renovated, zipcode, lat, long, sqft_living15 and sqft_lot15. 

I proceed to plot visualizaitons in relation to correlations using the heat map:
![graph1](./Images/heatmap.png)

Since we have a dependent variable price I decided to proced plotting relationship between price and other columns:
![graph1](./Images/plotvs.png)


* Missing values.
* Data type conversions.
* Checking for and removing multicollinearity.
* Normalizing our numeric data.
* Converting categorical data to numeric.
* Dropping Columns not relevant.
* Checking for outliers.


![graph1](./Images/unique_val.png)
![graph1](./Images/heatmap.png)
![graph1](./Images/outliers.png)
![graph1](./Images/3std.png)



Also could see more details in how the data is transform, clean, regression modeling and validation examination in `King County Housing Analysis.ipynb`.
## Summary

This project will give you a valuable opportunity to develop your data science skills using real-world data. The end-of-phase projects are a critical part of the program because they give you a chance to bring together all the skills you've learned, apply them to realistic projects for a business stakeholder, practice communication skills, and get feedback to help you improve. You've got this!
