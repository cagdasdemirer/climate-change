# Global Warning Project
![global-warning-dss.png](/global-warning-dss.png "DSS Diagram")
## Index
- notebook1.ipynb : Notebook where we make future predictions by analyzing past Co2 concentration and emission values ​​with ARIMA
- notebook2.ipynb : Notebook on which we predict the future temperature by calculating the CO2 values we already predict and technological variables.
- fc_all.csv : CO2 PPM Predictions, 2021-2063, 500*5, Monthly, Worldwide 
- fc_all2.csv : CO2 Emission Predictions, 2021-2065, 45*5, Annual, Worldwide
- co2_mm_cl.csv: Past CO2 Concentration Data, 1980-2021, 501*4, Monthly, Worlwide (It is processed by combining it with another dataset from the same source(statsmodels.api.datasets, 1958-2021))
Source:[Datahub.io](https://datahub.io/core/co2-ppm)
- global-co2-fossil-plus-land-use.csv: Past CO2 Emission Data, 1850-2020, 171*6, Annual, Worldwide
Source: [Global Carbon Project. (2021). Supplemental data of Global Carbon Budget 2021 (Version 1.0)](https://ourworldindata.org/co2-emissions#global-co2-emissions-from-fossil-fuels-and-land-use-change)
- GlobalLandTemperaturesByCountry.csv: Past Tempature Data, 1743-2013, 577462*4, Monthly, Worldwide (Grouped by Country)
Source: [Data.world](https://data.world/data-society/global-climate-change-data)
- formula.png : It is a one-dimensional climate forecast model produced by Dr.Randy M. Russell who works in University Corporation for Atmospheric Research.
Source: [ Climate Model](https://eo.ucar.edu/staff/rrussell/climate/modeling/co2_climate_model_activity.html)
- global-warning-dss.png : Decision Support System Diagram

![formula.png](/formula.png "Basic Model")
## Functions
```sh
app()
```
It is a DSS application that includes the calc_tempature function and interacts with the user and provides predictions. No input is required to call the  app() function. It is available in notebook2.ipynb.
```sh
calc_tempature(country, year, month, option1 = 0,option2 = 0,option3 = 0,option4 = 0,option5 = 0,option6 = 0)
```
It is a function that calculates the effect of variables on the values ​​obtained with our estimation model and presents it to the user as a report. It needs inputs such as country, year, month and the transition rates of various sectors to green technologies. While modeling how technological developments affect carbon emissions, Global Carbon Project 2010 Sectoral carbon emission percentages were taken as reference.