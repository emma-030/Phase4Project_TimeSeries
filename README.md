
# Top Zip Codes in Harris County for Real Estate Investment
## 1.0 Overview
A real estate investment company (client) is interested in investing in real estate in Harris County, Texas, USA. The client asked us to recommend the top five zip codes they can consider for investment. To enable us make this recommendation, we sourced a public dataset from Zillow that contains high volumes of historical house prices in the USA. We utilized Time Series analysis (SARIMA) to build a forecasting model to predict 3 years's worth of future house prices. With the predicted house prices, we calculated the expected return on investment (ROI) and recommended 5 zipcodes with the highest ROI.

## 2.0 Problem Statement
Our client is a small-medium real estate enterprise that wants to invest in Harris County for the first time. Our client does not have first hand experience and historical information about the housing prices and their projections for growth in this county. Our client has asked us to perform analysis on publicly available housing data and make recommendations on the top five zip codes for a potential investment.The client is interested in properties with an average cost of  USD 200000 to USD 300000 as at April 2018.
## 3.0 Project Objectives
The main goal and objectives for this project are:
1. Build a Time Series model that accurately forecasts future house prices
2. Determine & recommend the top 5 Zip codes for potential investment based on projected return on investment (ROI)
## 4.0 Findings from data analysis
### 4.1 Exploring cities & zipcodes in Harris County
From data analysis we observed that Harris county has more than 100 zipcodes. We need to recommend the top five only. The image below shows the distribution of zipcodes with Harris County cities; with house prices within clients planned budget.
![Cities_&_ZipCodes]('Cities_Zipcodes_Budget.png')

### 4.2 Historical prices & ROI in Harris County
Below we capture the general price trends in Harris County for houses under client budget. This shows that the county's prices have been on upward trend that accelerated post 2012. Its important to note that despite the subprime mortgage & financial crisis of 2008, Harris county's prices saw a minimal drop.
![Historical_Prices]('ZipCode_Prices.png')

Additionally, the average return on investment between 2012 and 2018 is attractive for investment given more than average market returns.
![Historical_ROI]('Historical_ROI.png')

### 5.0 Time Series Modelling
Our choice model for the project is Seasonal Auto-Regressive Integrated Moving Average (SARIMA). The decision was informed by studying the dataset and observing presence of regular intervals & patterns hence its ability to capture seasonal trends and analyze (& predict) long term market trends, hence suitability for time series analysis. Presence of seasonality further directed the decision to SARIMA.

### 5.1 Model 1 - SARIMA Model for sample zipcode
Given Harris county has more than 100 zipcodes, we created our first SARIMA model for 1 county (77080) to enable model performance observation, evaluation and fine tuning before deploying the model to all zipcodes.
![Model1_zip77080]('Zipcode_77080.png')

As per image above, the model almost perfectly captured the trend between 2012 and 2014. Between 2014 and 2018, our model is conservative resulting in lower forecast values as compared to the actual values.


We calculated the model's Root Mean Squared Error (RMSE) which came to USD 22,273.39. Given the average price in this zipcode is 300,000 (hence a loss of ~7%), we felt comfortable with the model's performance hence decision to go ahead and forecast future prices for for this zip code.
Zipcode 77080's 36 months' forecast:
![Model1_zip77080_forecast]('Zipcode_77080_forecast.png')

With our model's forecast not too far off from actual values, we decided to go ahead and forecast future prices for all zipcodes in Harris county, a duration of 3 years. See findings below

### 5.2 Final Model - SARIMA Model for all Zip codes in Harris County that are within the USD 200,000 to 300,000 client budget
Using the workflow established in Model 1, we forecasted a period of 36 months for all zipcodes in Harris county. 
Additionally, we calculated the ROI on the forecasted future price at end of April 2021. We sorted the future ROIs and plotted the top five zip codes per below:
![Top5_zipcodes]('Top5_zipcodes.png')

Our final model forecasted house prices for the future period between 2018 & 2021. Per image above, we see the predicted top 5 zip codes interms of highest ROI; i.e., zipcodes: 77092, 77003, 77062, 77586 and 77345 whose ROI in the next 3 years will be between 23% & 33%.
## 6.0 Recommendations & Conclusions

We recommend that our client invests in the top five zip codes listed below:
Zip Code Predictions:
1. Zip Code 77092: 33.09%
2. Zip Code 77003: 30.54%
3. Zip Code 77062: 23.13%
4. Zip Code 77586: 22.86%
5. Zip Code 77345: 21.81%