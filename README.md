# Predicting the Price of a Used Car
## Project Overview
* This project was completed as part of coursework for [The 365 Data Scicence Program](https://365datascience.com)
* Full project notebook: [Predicting the Price of a Used Car Jupyter Notebook](https://github.com/JonR45/Predicting-the-Price-of-a-Used-Car/blob/master/ML%20Project%20—%20Predicting%20the%20Price%20of%20a%20Used%20Car.ipynb)
* The goal of the project was to create a model that was able to accurately predict the price of used cars based on their specifications; the project required skills in the following areas: 
  * Machine Learning (Multiple Linear Regression)
  * Data Cleaning
  * Data Wrangling
  * Data Analysis
  * Data Visualisation
  * Statistical analysis
  * Problem Solving
  * Creative Thinking
  * Domain knowledge

## Code, Languages and Packages Used
**Python Version:** 3.7

**Packages:** numpy, pandas, statsmodels, matplotlib, scikit-learn, seaborn

**Data:** The raw data was provided by [365 Data Science](https://365datascience.com)

## Data Preprocessing
Exploring the descriptive statistics of the variables allowed me to make 3 key observations:
1. There were missing values.
2. One variable ('Model') had 312 unique entries.
3. The important variables were: Brand, Mileage, Engine Volume and Year of Production.

I was then able to drop the missing value entries before moving on to further explore the data.
## Exploratory Data Analysis
### Exploring the Probability Distribution Functions (PDFs)
* Analysis of the PDFs revealed that Price, Mileage, Engine Volume and Year of production all contained outliers.
* After this analysis I took the following action:
  * Removed the top 1% of observations for Price and Mileage
  * Removed observations >6.5 for Engine Volume (research suggested that Engine Volumes above 6.5L are rare and that 99.9 had been used when there was no entry)
  * Removed the bottom 1% of Year of Production
### Checking the Ordinary Least Squares Assumptions
* Checking the linearity assumption revealed that:
 1. Price did not have a linear relationship with the key varables)

![Linearity scatter plot](https://github.com/JonR45/Predicting-the-Price-of-a-Used-Car/blob/master/Images/Linearity%20scatter%20plot.png")

Thus, I performed a log transformation of Price: 

![Price transformed scatter plot](https://github.com/JonR45/Predicting-the-Price-of-a-Used-Car/blob/master/Images/Log%20Price%20scatter%20(price%20transformed).png)

2. Year was too correlated with other variables (Multicollinearity existed) and thus the 'Year' variable was dropped.

### Create Dummy Variables
I created dummy variables so that categorical variables could be included in the regression.

## Model Building and Testing
To build the model I did the following:
1. Declared the inputs and targets
2. Scaled the data
3. Split the data into train and test sets with an 80% training and 20% test split.
4. Created the multiple linear regression
5. Checked and interpretated the results. This included:
   1. Plotting the predicted values of the regression against the obsered values.
   2. Plotting the residuals and checking  for anomalies
   3. Finding the R squared, weights and bias.
6. Tested the Model
 1. Made the data easier to compare and interpreted the results

## Model Performance
![Test targets vs predicted targets](https://github.com/JonR45/Predicting-the-Price-of-a-Used-Car/blob/master/Images/Test%20targets%20vs%20predicted%20targets.png)

* The model is very good at predicting higher prices but not quite so good at predicting lower prices.
* The 25th, 50th and 75th percentile show that the predictions are reasonably close. 

## Summary
* The model is ok but can be improved; it is likely missing an important factor which drives the price of a used car lower. 
* It may be the model of the car which was removed at the beginning of the analysis but it could also be down to information not provided, such as whether or not there is any damage to the car and the severity of it, how many services and/or replaced parts the car has had, how many previous owners.
