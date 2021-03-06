# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Regression Challenge

### Contents:
- [Background](#Background)
- [Problem Statement](#Problem-Statement)
- [Datasets](#Datasets)
- [Data Dictionary](#Data-Dictionary)
- [Summary of Analysis](#Summary-of-Analysis)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background

Linear regression is a very popular model created from relationship between one target variable (or dependent variable) and one or more explanatory variables (independent variable). In this Regression Challenge, Aimes Iowa housing dataset is used to build a model with can predict the estimated sale price of each house. 

By obtaining the model, not only the price can be predicted, the importance of each features that affect the price can be investigated. With further analysis, this model can help sellers or anyone interesting in increasing their sale price to correctly make an improvement of their houses and obtain the highest price possible. 

## Problem Statement

**For customers who want to sell their house, what is an estimated current sale price ? 
And what should be any improvements that can raise the price up?**

## Datasets

In this challenge, the following files are used:

* [`train.csv`](/datasets/train.csv): training data of Aimes Iowa Housing containing 2051 rows and 81 columns while each row represents a house sold and each columns represent characteristic of that house.. 
* [`test.csv`](/datasets/test.csv): testing data for the model built in this challenge. 

This data set contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010. The data set is published by Ames, Iowa Assessor’s Office .

## Data Dictionary

| Feature       | Type  | Description                                                            |
|---------------|-------|------------------------------------------------------------------------|
| SalePrice     | int   | the property's sale price in dollars                                   |
| MSSubClass    | int   | The building class                                                     |
| MSZoning      | str   | Identifies the general zoning classification of the sale               |
| LotFrontage   | float | Linear feet of street connected to property                            |
| LotArea       | float | Lot size in square feet                                                |
| Street        | str   | Type of road access to property                                        |
| Alley         | str   | Type of alley access to property                                       |
| LotShape      | str   | General shape of property                                              |
| LandContour   | str   | Flatness of the property                                               |
| Utilities     | str   | Type of utilities available                                            |
| LotConfig     | str   | Lot configuration                                                      |
| LandSlope     | str   | Slope of property                                                      |
| Neighborhood  | str   | Physical locations within Ames city limits                             |
| Condition1    | str   | Proximity to main road or railroad                                     |
| Condition2    | str   | Proximity to main road or railroad (if a second is present)            |
| BldgType      | str   | Type of dwelling                                                       |
| HouseStyle    | str   | Style of dwelling                                                      |
| OverallQual   | int   | Overall material and finish quality                                    |
| OverallCond   | int   | Overall condition ratin                                                |
| YearBuilt     | int   | Original construction date                                             |
| YearRemodAdd  | int   | Remodel date (same as construction date if no remodeling or additions) |
| RoofStyle     | str   | Type of roof                                                           |
| RoofMatl      | str   | Roof material                                                          |
| Exterior1st   | str   | Exterior covering on house                                             |
| Exterior2nd   | str   | Exterior covering on house (if more than one material)                 |
| MasVnrType    | str   | Masonry veneer type                                                    |
| MasVnrArea    | float | Masonry veneer area in square feet                                     |
| ExterQual     | str   | Exterior material quality                                              |
| ExterCond     | str   | Present condition of the material on the exterior                      |
| Foundation    | str   | Type of foundation                                                     |
| BsmtQual      | str   | Height of the basement                                                 |
| BsmtCond      | str   | General condition of the basement                                      |
| BsmtExposure  | str   | Walkout or garden level basement walls                                 |
| BsmtFinType1  | str   | Quality of basement finished area                                      |
| BsmtFinSF1    | float | Type 1 finished square feet                                            |
| BsmtFinType2  | str   | Quality of second finished area (if present)                           |
| BsmtFinSF2    | float | Type 2 finished square feet                                            |
| BsmtUnfSF     | float | Unfinished square feet of basement area                                |
| TotalBsmtSF   | float | Total square feet of basement area                                     |
| Heating       | str   | Type of heating                                                        |
| HeatingQC     | str   | Heating quality and condition                                          |
| CentralAir    | str   | Central air conditioning                                               |
| Electrical    | str   | Electrical system                                                      |
| 1stFlrSF      | float | First Floor square feet                                                |
| 2ndFlrSF      | float | Second floor square feet                                               |
| LowQualFinSF  | float | Low quality finished square feet (all floors)                          |
| GrLivArea     | float | Above grade (ground) living area square feet                           |
| BsmtFullBath  | int   | Basement full bathrooms                                                |
| BsmtHalfBath  | int   | Basement half bathrooms                                                |
| FullBath      | int   | Full bathrooms above grade                                             |
| HalfBath      | int   | Half baths above grade                                                 |
| Bedroom       | int   | Number of bedrooms above basement level                                |
| Kitchen       | int   | Number of kitchens                                                     |
| KitchenQual   | str   | Kitchen quality                                                        |
| TotRmsAbvGrd  | int   | Total rooms above grade (does not include bathrooms)                   |
| Functional    | str   | Home functionality rating                                              |
| Fireplaces    | int   | Number of fireplaces                                                   |
| FireplaceQu   | str   | Fireplace quality                                                      |
| GarageType    | str   | Garage location                                                        |
| GarageYrBlt   | int   | Year garage was built                                                  |
| GarageFinish  | str   | Interior finish of the garage                                          |
| GarageCars    | int   | Size of garage in car capacity                                         |
| GarageArea    | float | Size of garage in square feet                                          |
| GarageCond    | str   | Garage condition                                                       |
| PavedDrive    | str   | Paved driveway                                                         |
| WoodDeckSF    | float | Wood deck area in square feet                                          |
| OpenPorchSF   | float | Open porch area in square feet                                         |
| EnclosedPorch | float | Enclosed porch area in square feet                                     |
| 3SsnPorch     | float | Three season porch area in square feet                                 |
| ScreenPorch   | float | Screen porch area in square feet                                       |
| PoolArea      | float | Pool area in square feet                                               |
| PoolQC        | str   | Pool quality                                                           |
| Fence         | str   | Fence quality                                                          |
| MiscFeature   | str   | Miscellaneous feature not covered in other categories                  |
| MiscVal       |       | $Value of miscellaneous feature                                        |
| MoSold        | u     | Month Sold                                                             |
| YrSold        | int   | Year Sold                                                              |
| SaleType      | str   | Type of sale                                                           |



## Summary of Analysis


## Conclusions and Recommendations

