# Predicting the Price of a Used Car
## Project Overview
* This project was completed as part of coursework for [The 365 Data Scicence Program](https://365datascience.com)
* Project in Jupyter Notebook: [Predicting the Price of a Used Car Jupyter Notebook]()
* The goal of the project was to create a model that was able to accurately predict the price of used cars based on their specifications; the project required the following skills: 
  * Machine Learning (Multiple Linear Regression)
  * Data Cleaning
  * Data Wrangling
  * Data Analysis
  * Data Visualisation
  * Statistical analysis
  * Problem Solving
  * Creative Thinking
  * Domain knowledge

### Code, Languages and Packages Used
**Python Version:** 3.7
**Packages:** numpy, pandas, statsmodels, matplotlib, scikit-learn, seaborn

### Data Preprocessing
Exploring the descriptive statistics of the variables allowed me to make 3 key observations:
1. There were missing values.
2. One variable ('Model') had 312 unique entries.
3. The important variables were: Brand, Mileage, Engine Volume and Year of Production.

I was then able to identify and deal with missing values; missing values constituted <5% of the data, thus these entries were dropped)

### Exploratory Data Analysis
#### Exploring the Probability Distribution Functions (PDFs)
* Analysis of the PDFs revealed that Price, Mileage, Engine Volume and Year of production all contained outliers.
* After this analysis I took the following action:
  * Removed the top 1% of observations for Price and Mileage
  * Removed observations >6.5 for Engine Volume (research suggested that Engine Volumes above 6.5L are rare and that 99.9 had been used when there was no entry)
  * Removed the bottom 1% of Year of Production
#### Checking the Ordinary Least Squares Assumptions
* Checking the linearity assumption revealed that price did not have a linear relationship with the key varables: 



### Model Building
Info about the model

### Model Performance
Error rates, accuracy and other information about the predictions

### Results and Conclusions
Notes about real-world usage of the model
Link to Jupyter Notebook
