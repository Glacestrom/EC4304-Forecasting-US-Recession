# EC4304 - Forecasting the Next US Recession
## Disclaimer
While this project was a collaborative group effort, I want to emphasize that all the Python codes (including the XGBoost model) was entirely my own work and is self-contained. As the other aspects of the project were conducted using Stata, no additional code is necessary to reproduce the results of the XGBoost model. Should you have any queries or need further information, please don't hesitate to get in touch. Thank you for your understanding.
## Introduction
Following Kauppi and Saikonnen (2008)’s model with the US interest rate spread data, we developed dynamic binary probit/logit models for predicting U.S. recessions using the interest rate spread & lags of the recession binary variable as the driving predictors with gradient boosting.
## Data Source
Data for this analysis was taken from the Federal Reserve Economic Data (FRED) online database, a comprehensive resource with sufficient data on US economic indicators (Mendez-Carbajo & Podleski, 2021).  
Our starting date was 1953 April which is the earliest date with data for 10-Year Treasury Bills. We partitioned our test set to include 3 recession periods: the Early 2000s Recession, the 2007-2008 Global Financial Crisis, and the 2020 COVID-19 Recession.   

Target Variable: Binary US Recession Indicator (USREC)

Independent Variables:
- Lags 12 - 18 of US Recession Indicator (USREC)
- Lags 1 - 18 of Interest Rate Spreads:
  - 10-Year minus 3-month rate (GS10 - TB3MS)
  - 5-Year minus 3-month rate (GS5 - TB3MS)
  - 1-Year minus 3-month rate (GS1 - TB3MS)
  - High Yield Spread of Junk Bonds (BAA - AAA)  

Train Set Period: 1953 April to 2000 December (573 Samples)  
Test Set Period: 2001 January to 2022 September (261 Samples)

## Setting Up
1. Download the files
2. Install the required packages
3. Run the codes
