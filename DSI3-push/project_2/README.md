# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)Project 2: Ames Housing Data Analysis

#

### GA Project 2

### Table of content
- Problem Statement
- EDA & Cleaning
- Feature Engineering
- Modeling 
- Kaggle Submission
- Conclusions

### Problem Statement

### Who we are?
A group of real estate analysts in Iowa that works for a private real estate institution 

### The real problem
As real estate analysts in Iowa, we are responsible for managing our organization's real estate holdings.

We are tasked with understanding real estate market trends and to minimize current and future real estate holding risks.

We will be conducting data analysis on the Iowa real estate market and determine which are the factors that affects property prices.

The purpose of this analysis is to better understand a property price and provide suitable insights to management and potential buyers of the organization's real estate.


This studies is on what feature is most correlated to saleprice for the house in Iowa.
---

# Tools and Libraries Used:
python, pandas, numpy, seaborn, matplotlib, scikit-learn

Dataset of housing prices in Ames, Iowa from 2006 to 2010. As such, the data dictionary provides a thorough breakdown of the variables involved.

Here are some of the features:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**id**|*int*|*train*|Property number
|**pid**|*int*|*train*|Row number
|**ms_subclass**|*int*|*train*|The building class
|**ms_zoning**|*string*|*train*|Identifies the general zoning classification of the sale.
|**lot_frontage**|*float*|*train*|pathway connected to property
|**lot_area**|*int*|*train*|lot size in square foot
|**street**|*string*|*train*|pathway connected to road
|**alley**|*string*|*train*|alley connected to property
|**lot_shape**|*string*|*train*|General shape of property
|**land_contour**|*string*|*train*|Flatness of the property
|**utilities**|*string*|*train*|Type of utilities available
|**lot_config**|*string*|*train*|Lot configuration
|**land_slope**|*string*|*train*|Slope of property
|**neighborhood**|*string*|*train*|Physical locations within Ames city limit
|**exterior_1**|*string*|*train*|Exterior covering on house
|**exterior_2**|*string*|*train*|Exterior covering on house
|**mas_vnr_type**|*string*|*train*|Masonry veneer typ
|**mas_vnr_area**|*float*|*train*|Masonry veneer area in square feet
|**misc_val**|*int*|*train*|General $Value of miscellaneous feature
|**mo_sold**|*int*|*train*|Month Sold
|**yr_sold**|*int*|*train*|Year Sold
|**sale_type**|*string*|*train*|Type of sale
|**saleprice**|*int*|*train*|Price property was sold at

---
### Data Analysis
![image.png](https://i.postimg.cc/zDpjvbVc/Untitlwqeed.png)
![image.png](https://i.postimg.cc/GhFbvRnV/Untitled.png)
---
### Modelling
![image.png](https://i.postimg.cc/kG5WKsBh/Untit3led.png)
---
### Kaggle score = 1595743.51
### Conclusions & recommendations
In order to have a model that predict the price of house accurate first we will need to clean up our data with the help of EDA, where we will be looking at data  imputation of the null values, convertion of discrete, continous, ordinal and nominal values in variables, identifying which are the outlier. Adding in features engineering , followed by modelling our data modified. 
 
Some recommendations:
- lasso is suited the best for the housing price prediction.
- Highest R2 score = 0.9451
- Most suitable to be used at the same district or city area.
