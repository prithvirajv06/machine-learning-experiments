# AUS Building Price predection

## Problem Statement

A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

## Inferance

From all the above we can see The higher values of positive coeeficients suggest a high sale value

Ridge Regression was better in terms of R2 values of Train and Test,it is better to use Lasso


Selected  Feature	and  Description
- GrLivArea	Above grade (ground) living area square feet
- OverallQual	Rates the overall material and finish of the house
- OverallCond	Rates the overall condition of the house
- TotalBsmtSF	Total square feet of basement area
- GarageArea	Size of garage in square feet

Age and MSSubClass are deciding the reduced value in sale price