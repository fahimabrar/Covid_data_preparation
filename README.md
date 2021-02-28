#### Data preaparatin for Covid Spred time series analysis

##### Notes: 
- this master data is collected from several sources
- Please go to the original link to see the liscence of the original dataset
- For latest data download the latest dataset from the given link, some data updated daily
- In data preparation folder all the notebooks can be used for data preparation

##### Original Data Source
- Bing covid data - [Microsoft Bing](https://github.com/microsoft/Bing-COVID-19-Data/tree/master/data)
- Air Passenger data - [The OPENSKY Network 2020](https://zenodo.org/record/4485741)
- Airport data - [Open Flights](https://openflights.org/data.html)
- Financial Measure data - [World Bank](https://datacatalog.worldbank.org/dataset/covid-19-finance-sector-related-policy-responses)
- Population data - [World Bank](https://data.worldbank.org/indicator/SP.POP.TOTL)
- Land Area data - [World Bank](https://data.worldbank.org/indicator/AG.LND.TOTL.K2)
- GDP data - [World Bank](https://data.worldbank.org/indicator/NY.GDP.MKTP.CD)

##### Data Description
- This Master dataset is a time series dataset of covid spread along with number of flights landed on a particular country
- It also has demographic feature of the country


|Column header | Description | 
|---|---|
|Updated| Datetime in UTC |
|Confirmed | Confirmed case count for the region |
|ConfirmedChange| Change of confirmed case count from the previous day |
|Deaths| Death case count for the region |
|DeathsChange| Change of death count from the previous day |
|Recovered| Recovered count for the region |
|RecoveredChange| Change of recovered case counts from the previous day |
|Country Name| Full name of the country |
|Number of Flights| Number of flights landed on that day |
|GDP | Country’s gross domestic product |
|Land Area| Country’s land area in sq. km |
|Population| Country’s total population |
|Income Level| Income level of the country|



##### Data Preparation

**Air Passenger** data cleaning
 We callected aeroplane movement data for 2020 (12 datasets). For each day it has origing and destination ICAO code of the airport. Each day an ICAO occurs in a destination columns means an aeroplane landed in that airport. 
 
 In our covid dataset we have country name, not airport name. So we need to convert ICAO into country name. [The OPENSKY Network 2020](https://zenodo.org/record/4485741) dataset has data of ICAO and country name. So, we merge (left merge air passenger data with icao-country data) both dataset on ICAO column and get the country name for each ICAO. 
 
Still in our dataset each row means an aeroplane movement. But we need number of aeroplane movement in a specific country. SO we group them by country name and data and measure the count. Now we get 28 or 30 or 31 rows for a month for each country. We do the same operation for the 12 months. And after that we concatinate all the 12 datasets and get a master dataset that contains each day aeroplane movement count for each country. We also convert date format so that it matches with covid dataset date format. 


 **Country** data cleaning
 In country data we basically want the demographic and economic condition of each country. We merge gdp, landarea, financial data and population data together based on country name. In some country name there was some whitespace, that was removed. Otherwise it doesnot merge properly.
 
 
 **Master Dataset** creating
 We merge covid data with air passenger movement and country data based on date and country name and created our master dataset. 


##### And
- In data preparation folder all the jupyter notebook uploaded that used for data preparation, cleaning, merging etc. 
- The notebook written with enough commenting and doucumentation
- Some dataset are more than 1 GB, so for memory limit of github, we cannot upload. But link to original dataset provided 

**Thank You**




