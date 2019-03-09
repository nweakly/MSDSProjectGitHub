#  Predicting Denver Traffic Accidents using machine learning techniques in Python

## Project Overview

The number of car accidents in Denver has been steadily increasing over the past few years. While almost everyone agrees that human costs in terms of lost lives and injuries are unacceptable and that economic consequences, for example, high car insurance premiums, are felt by many, there is no consensus on what factors are driving this trend. So, I came up with this exploratory project;  its main goal is to analyze car accident data for the last 5 years in order to try to find variables that can be used as predictors for future car accidents.

![Accidents 2014-2018](https://github.com/nweakly/MSDSProjectGitHub/blob/master/AnnualNumberOfAccidents.GIF "Car Accidents, Denver, CO 2014 - 2018")

In casual conversations and on social media people often mention at least four stereotypical reasons for growing number of accidents –  explosive population growth  due to out of state migration, alcohol consumption, recreational marijuana use and drugs in general, and everchanging Colorado weather. So, in this project, I would like to assess the validity of these claims. 

![Map of the reaffic accidents, 2018](https://github.com/nweakly/MSDSProjectGitHub/blob/master/IndividualAccidents.GIF "Location of traffic accidents in Denver, CO (2018)")

The main source of accidents data for this project is the traffic accident dataset maintained by the City and County of Denver Police Department. It contains data about all accidents with reported damage more than 1ooo dollars or involving fatalities, injuries or evidence of drug or alcohol use for the past 5 years. It is a dynamic dataset, it is updated every workday, including refining information about previously reported incidents. When I downloaded it for my project, it contained 164116 observations of 20 variables.  Additional sources of information included data about retail alcohol and recreational marihuana sales in the state of Colorado, monthly employment statistics (as a proxy for population data), weather observations and others.

Due to the scope of the project and the amount of data preprocessing, it was split into several jupyter notebook files with interim results saved as csv files, so each stage of the project can be run independently from others. 

## EDA (Exploratory Data Analysis)

Please see MSDSProjectGitHub/MSDS692_trafficAccidents.ipynb file.
      
## Implementation

### Data collection and preprocessing:
Please see: 
- MSDS692_AlcoholSales.ipynb
- MSDS692_Holidays.ipynb
- MSDS_LaborForce.ipynb
- MSDS692_MJSales.ipynb
- MSDS692_SunriseSunsetData.ipynb
- MSDS692_WeatherData.ipynb

### Merging data and preparing for ML:
- MSDS692_IndividualAccidents.ipynb
### ML models  and discussion of the results:
- Linear Regression: MSDS692_MonthlyAccidents.ipymb
- KMeans Clustering: MSDS692_Clustering.ipynb
- ANN: MSDS692_Forecasting.ipynb
- Time Series Analysis: MSDS692_TimeSeries.ipynb

## Conclusions

While this project has not resulted in building a robust predictive model, I think it still provided some important insights into the situation with car accidents in Denver:

- Car accidents in Denver cannot be reliably predicted exclusively based on population growth, alcohol, and recreational marijuana use, or weather conditions. Traffic accidents in Denver are a complex phenomenon that cannot be reduced to stereotypical factors.
- To increase the predictive power of the models, we need to include other factors (e.g., traffic patterns, fleet characteristics, driver behavior (e.g, estimated by the number of speeding tickets issued), enforcement practices etc.).
- Need to reevaluate assumptions and include more granular and precise data (e.g., road surface conditions not just weather observations).
- Not all algorithms are equally suitable for the task (e.g., K-means was only able to pick up day-of-the-week differences), need to use a different approach to clustering.
- Unexpectedly, time series analysis provided the most precise prediction. I was expecting the neural network to be better suited, but it is most likely can be explained by the choice of independent variables.
- Note to myself for future projects: building datasets from scratch takes time and might be not the best solution for a time-restricted school project. 
- In order to improve my python programming skills I used it exclusively throughout the project, otherwise, some particular tasks can be more efficiently accomplished using other DS tools (e.g., time series analysis seems to be easier in R).

# References
Video presentation for this project: https://www.youtube.com/watch?v=Lj7lx8ZfaRE 

