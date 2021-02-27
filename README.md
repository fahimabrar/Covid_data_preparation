#### Data preaparatin for Covid Spred time series analysis

##### N:B: 
- this master data is collected from several sources
- Please go to the original link to see the liscence of the original dataset

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
- In data preparation folder all the jupyter notebook uploaded that used for data preparation, cleaning, merging etc. 
- The notebook written with enough commenting and doucumentation
- Some dataset are more than 1 GB, so for memory limit of github, we cannot upload. But link to original dataset provided

