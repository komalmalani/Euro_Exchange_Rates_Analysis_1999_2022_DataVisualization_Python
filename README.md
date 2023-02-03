# Project Details
The dataset we'll use describes Euro daily exchange rates between 1999 and 2021. The euro (symbolized with €) is the official currency in most of the countries of the European Union.
If the exchange rate of the euro to the US dollar is 1.5, you get 1.5 US dollars if you pay 1.0 euro (one euro has more value than one US dollar at this exchange rate).
My role being an analyst is :
-- To analyze exchange rates for Euro_to_US has changed over period of 30 years.
-- EURO_USD rate change between 1999 and 2021 with 30days Moving Average
-- EURO_USD rate change during Coronavirus Pandemic¶
-- EURO_USD rate fluctuations during "The Three US Presidencies " , so on and so forth

![1](C:\Users\komal\OneDrive\Desktop\DataJourney\projects\Python-Projects\Euro_Exchange_DailyRates_1999_2022\Euro_dollar.png)

# Data
The data source is the European Central Bank. Daria Chemkaeva put together the data set
and made it available on [Kaggle](https://www.kaggle.com/datasets/lsind18/euro-exchange-daily-rates-19992020)  

# What are the steps followed?
1.	Read in the sv file into a pandas DataFrame 
2.	Inspect the first and the last five rows to understand the structure of the dataset.
3.	Use the DataFrame.info() method to learn some basic facts about the dataset:
-- What is the number of rows and columns?
-- Are there null values?
-- What is the data type of each column?

## Data Cleaning
-- Rename the [US dollar] and Period\Unit: columns to something easier to type — US_dollar and Time.
-- Change the Time column to a datetime data type.
-- Sort the values by Time in ascending order.
-- Reset the index (and drop the initial index)
-- Isolate the Time and the US_dollar columns and assign them to a different dataframe euro_to_dollar.
-- Ran the Series.value_counts() method on the US_dollar column, found out some columns have "-".
-- Drop all the rows where the - character appears in the US_dollar column.
-- Convert the US_dollar column to a float data type.

## Data Analysis
- Tried to make plots showing original values, rolling mean of where rolling windows is 7, 30 and 50,100 and 365 days
- Covid Pandemic : had a closer look to the more specific period of time and explore how the euro-dollar rate has changed during the Coronavirus Pandemic. The 2020 data will be shown and the 2016-2019 data will be used as a baseline.
- Euro-Dollar rate fluctuations during "The Three US Presidencies"
