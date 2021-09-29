# Case_Study_1


# Introduction
​
This analysis is for a Capstone Project from the Google Data Analytics Certificate. The project is based on the case study "Sophisticated, Clear, and Polished: Divvy and Data Visualization" written by Kevin Hartman (found here: https://artscience.blog/home/divvy-dataviz-case-study). We will be using the Divvy dataset for our analysis. This project aims to collect, prepare, process, and analyze our given data source. Then share our data insights and visualizations to answer the key business question the scenario: "In what ways do the members and the casual riders use Divvy bikes differently?"
​
# Scenario
​
In the given scenario, I am a data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company's future success depends on maximizing the number of annual memberships. My team aims to understand how casual riders and annual members use Cyclistic bikes differently. These insights will help the marketing team design a new marketing strategy to convert casual riders into annual members.
​
**Key Stakeholders:**
​
* Primary Stakeholders - the director of marketing
* Secondary Stakeholders - the marketing analytics team and the executive team
​
**Business Task**
​
Analyze the Cyclistic’s historical trip data from the past 12 months to identify trends that differ between annual members and casual riders.
​
# Preparing Data For Exploration:
​
**Data Sources:**
​
The datasets used for this analysis are made available by Motivate Internation Inc. under this [licence](https://www.divvybikes.com/data-license-agreement). 
​
[Data Source link](https://divvy-tripdata.s3.amazonaws.com/index.html)
​
The data source is public and can be used to explore the different customer types. 
​
**Notes:** 
​
* The data privacy issues prohibit us from using riders’ personally identifiable information meaning that we can not connect past purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or have purchased multiple passes.
​
* Cyclistic is a fictional company; hence the datasets contain the name of a different company. For this analysis, the given datasets can be used for our business task.
​
* The period analyzed is 12 months, from August 01, 2020, to September 31, 2020. 
​
* The data being souced can be relied on as the datasets are comprehensive, recent and initially sourced by Motivate Internation In, and appropriately licenced and cited. 
​
**List of Datasets:**
​
* 202009-divvy-tripdata 
* 202010-divvy-tripdata
* 202011-divvy-tripdata
* 202012-divvy-tripdata
* 202101-divvy-tripdata
* 202102-divvy-tripdata
* 202103-divvy-tripdata
* 202104-divvy-tripdata
* 202105-divvy-tripdata
* 202106-divvy-tripdata
* 202107-divvy-tripdata
* 202108-divvy-tripdata
```{r}
install.packages("tidyverse")
library(tidyverse)
library(lubridate)
library(ggplot2)
library(dplyr)
install.packages("sqldf")
library(sqldf)
```


```{r}
library(readr)
X202009_divvy_tripdata <- read_csv("~/Project_1/202009-divvy-tripdata.csv")
View(X202009_divvy_tripdata)
X202010_divvy_tripdata <- read_csv("~/Project_1/202010-divvy-tripdata.csv")
View(X202010_divvy_tripdata)
X202011_divvy_tripdata <- read_csv("~/Project_1/202011-divvy-tripdata.csv")
View(X202011_divvy_tripdata)
X202012_divvy_tripdata <- read_csv("~/Project_1/202012-divvy-tripdata.csv")
View(X202012_divvy_tripdata)
X202101_divvy_tripdata <- read_csv("~/Project_1/202101-divvy-tripdata.csv")
View(X202101_divvy_tripdata)
X202102_divvy_tripdata <- read_csv("~/Project_1/202102-divvy-tripdata.csv")
View(X202102_divvy_tripdata)
X202103_divvy_tripdata <- read_csv("~/Project_1/202103-divvy-tripdata.csv")
View(X202103_divvy_tripdata)
X202104_divvy_tripdata <- read_csv("~/Project_1/202104-divvy-tripdata.csv")
View(X202104_divvy_tripdata)
X202105_divvy_tripdata <- read_csv("~/Project_1/202105-divvy-tripdata.csv")
View(X202105_divvy_tripdata)
X202106_divvy_tripdata <- read_csv("~/Project_1/202106-divvy-tripdata.csv")
View(X202106_divvy_tripdata)
X202107_divvy_tripdata <- read_csv("~/Project_1/202107-divvy-tripdata.csv")
View(X202107_divvy_tripdata)
X202108_divvy_tripdata <- read_csv("~/Project_1/202108-divvy-tripdata.csv")
View(X202108_divvy_tripdata)
```



