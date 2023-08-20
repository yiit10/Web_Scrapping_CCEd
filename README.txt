
# Data Analysis with R: Clergy Database Analysis

This repository contains R code for analyzing data from the Clergy Database. The analysis includes data scraping, cleaning, and various statistical modeling techniques.

## Setup

Before running the code, make sure you have the required R packages installed:

```R
library(data.table)
library(ggplot2)
library(parallel)
library(httr)
library(readxl)
library(RSelenium)
library(rvest)
library(dplyr)
library(tidyr)
library(fixest)
library(randomForest)
library(vtable)
library(huxtable)
library(caret)
```

Also, set your working directory to the appropriate location, where you put the following csv files:

CCED_web.csv
Population_England.csv
Transfer_Pop_CCED.csv

and using setwd at line 24, please specify the location to the code.

```R
setwd("")
```

If you want to use the web-scrapping code, please change eval = TRUE at line 56.
You can directly knit the code to see the results.

## Data Collection - Web Scraping

To collect data, web scraping is used through the RSelenium package. The data is collected from the [Clergy Database](https://theclergydatabase.org.uk/). The code for web scraping is provided in the `data-webscrapping` section. Please note that the data has been previously collected and saved in a CSV file for further analysis.

## Data Cleaning

The collected data is cleaned and prepared for analysis. Duplicate entries are removed, and data is filtered based on specific criteria. The `data_cleaning` section contains the code for this data cleaning process.

## Statistical Analysis

The code includes several statistical analyses using various modeling techniques:

### Ordinary Least Squares (OLS) Model

An OLS regression model is built to predict `max_pop` using predictor variables such as `nobs`, `year`, `lat`, `lon`, `latlon`, and `tt`.

### Random Forest Model

A random forest model is trained to predict `max_pop` using a subset of predictor variables.


For questions or further information, please contact F. Yiğit Kavak from fyigitkavak@icloud.com.