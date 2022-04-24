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

###  Background
We are a group of real estate analysts. Our project, would consist the Ames housing data to create a regression model that can predict the property price and provide suitable insights to management and potential buyers of the organization's real estate.

### Problem Statement

**What our plan are**

There are many variables that can determine how much a home can be priced at.

Using the Ames dataset, we want to determine which variables is affecting home saleprices the most and produce accurate saleprice predictions.

**What type of models will we be looking at?**

We will be focusing on supervised machine learning models. Linear, Lasso and Ridge Regression are areas we will be exploring.


**How will success be concluded?**

Our main focus is optimising 𝑅2 and RMSE for the different models. Our aim is to create a model that significantly outperforms the baseline model which we've identified.

**Is this the scope of the project appropriate? Who are our important stakeholders and why is this important to investigate?**

With our procedure mention above, models we have would provide insights for potential home-buyers, housing owners and our origanization stakeholders.

As real estate analysts in Iowa, we are responsible for managing our private real estate organization's real estate holdings.Thus, we are tasked with understanding real estate market trends and to minimize current and future real estate holding risks.

---

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

### Methodology

**EDA and Data Cleaning**

Our train dataset has a total of 81 columns. 
After rename feature to lowercase and _ names which are easier to work with. we dealt with smaller missing values variables.

**Addressing Missing values**

After which imputing missing values in qualitative features. Lot Frontage, Basement, Garage and filling up the rest with None.

Followed by checking null value correction. 

**Ordinal vs Catergorical**

I decided to tackle the project from another point of view, where I consider oridinal variables as a ranking thus I did not include One-hot encoding. 

Similar steps will be applied for our test dataset.
---
### Data Analysis
Pairplot of top correlation coefficient values
![image.png](https://i.postimg.cc/zDpjvbVc/Untitlwqeed.png)
![image.png](https://i.postimg.cc/GhFbvRnV/Untitled.png)

lastly, dealing with outlier (Taking a closer look at gr_liv_area, total_bsmt_sf, 1st_flr_sf
, these property are indeed the outliers hence choosing to remove them) and exporting to csv format.

---
### Modelling

![image.png](https://i.postimg.cc/kG5WKsBh/Untit3led.png)

### Baseline Score ###
My baseline score is base on Ridge Regression
RMSE: 22939
R2: 0.93

### --- 

### Kaggle score = 1595743.51

### Conclusions & recommendations
According to my model, Mas_vnr_area, total sf and bsmtfin_sf_1 has the highest coefficient of the model. This would impact our sale price as for example, every one change of Mas_Vnr_area coefficient it will affect the sales price by 7000. These are my top 3 highest coefficient that affect my propeties prices, and thus when we recommend to our housing owners we suggest that they focus on bsmtfin_sf_1 as all houses are allocated a fixed plot of land which cannot be increase easily. However, the 3rd highest coefficient would be bsmtfin_sf_1, according to my model we would recommend our housing owner to complete their basement before selling as this can greatly impact the propeties price of their houses. 

Through our model, we find that many of our clients who we have recommended to finishing their basement. They have sold their propeties at higher prices which inturn reflect more sale revenue for our organization in the past year. 

Future steps to improve the model:
According to my Feature Engineering, my RMSE score was not very good although I feel that some future possible steps to take that would improve my current model would be: One-hot encoding the Ordinal & Categorical variables.

Further elaborate, by One-Hot encoding all the Categorical Data, the model could have gotten a much better RMSE Score. Instead of changing categorical data to ordinal data which resulted in RMSE score of 22939.


