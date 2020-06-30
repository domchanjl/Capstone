# Kaggle Submission
## COVID-19 and Week 4 Kaggle Challenge
---
### Problem Statement

The COVID-19 pandemic is defining global health crisis in our time. This has been the greatest threat to humanity since SARS (Severe Acute Respiratory Syndrome). The virus spread quickly and widely, with cases is rising daily as the global effort to slow its spread is underway. Through her experiences with the SARS crisis, Singapore acted swiftly and decisively, implementing a proactive, nationwide lockdown, with the goal of flattening the curve. Notwithstanding, the other South East Asian Nations may yet have the resources and strategies to dealing with this situation. This project seeks to predict the global COVID-19 cases to accurately provision time for planning and resource responses.

Determining the significance of variables to accurately predict the global COVID-19 cases; to effectively predict their eventual progression of deaths and cases by means of the Regression models. This is to ensure that global citizens are made aware to the situation's progression and can make the necessary preparations should there be an extended lockdown period. goverenments and private companies can leverage on this model to make a informed decision as to growth of the economy and businesses.

Although a training (train.csv) and test (test.csv) dataset was provided, i attempted to scrape the data and clean it in a similar format to that of the Kaggle datset, ultimately comparing predictions. The target variable (Confirmed cases/Fatalities) were only available to the kaggle training set. The challenge was generating a regression model using the training data, to predict values of the target feature using the test data. The predictions were submitted to the Kaggle competition to be scored against the actual target values.

Root Mean Squared Error was the choice metric to judge the best performing model initially. Eventually, Kaggle measured success of the model against the lowest Root Mean Squared Log Error. 

---
### Executive Summary


- Data Gathering
- Exploratory Data Analysis
- Modelling
- Final Analysis

---
### My Process

#### Gathering the Data

The global datasets comes from the GitHub data repository for the 2019 Novel Coronavirus Visual Dashboard operated by the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE). This is also the source for the Kaggle competition dataset. In this part of the project, we go through with EDA on the data prepared.

The data was collected from 2 sources:

1. Global data (source updates this on a daily basis):
https://github.com/CSSEGISandData/COVID-19
2. Singapore data (source updated this daily, however search tab was last updated 19 Apr 2020):
https://co.vid19.sg/singapore/dashboard.

No API or loop was needed to collect the data.

#### EDA

The graphical plots enabled me to visually scan the data for possible relationsips between features. Top 10 countries with the most cases were different to those of deaths and recoveries. Scoping into ASEAN countries, we observe certain recovery for Brunei, Cambodia, Malaysia Thailand, Vietnam, with their efforts closest to "flattening the Curve". Countries with uncertain recovery include Laos and Singapore, with recovery rates not yet high enough but are hopeful to be "flattening". Burma (Myanmar), Indonesia, and Philippines showing very few recoveries or at a rate similar to those of deaths. Singapore data was also closely examine for age, nationality, means of transmission, etc. 

---
#### Modeling

3 regression technique were used to determine the best forecast for the COVID-19 spread; Linear Regression, Random Forest regression and eXtreme Gradient Boosting regression. Root Mean Squared Error was the chosen metric to judge the best performing model. in the experiment with the data i had gthered from the source url, the linear regression model performed worst on the training set but best on the test. On the Kaggle datasets, however, it was observed that random forest regressor was the best performing model. 

Upon submission to kaggle, i had a score of 0.68772, ranking this model in the top 230 spots for predictors at that time.

---
#### Further Improvements

i was conflicted as to why the kaggle dataset allowed my models to perform better than with the data i gathered. Despite having generated a relatively reliable predictive model, the following changes can still be made to better it:

- The current datasets have very little features to work with which led to me breaking up the datetime aspects of it to be used as engineered features.
- The data could be supplemented with additional features like weather info, public transport info, global events with participation rates and locations (i.e. music festivals/olympics). 


---
### Recommendation

The model can serve as a prediction model for countries and businesses. Additionally, citizens can be more discerning of the potential for number of cases and deaths to rise (or fall) with time.

Notwithstanding this, more data, as mentioned above, will serve to optimise the model. The model can also serve as a starting point, to be extrapolated to individual countries with additional research to be done marrying the features together.
