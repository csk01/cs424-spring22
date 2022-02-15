# Krishnan Chelakkarai Sivaraman
## CS424 - Project-1 - Subway  

## Introduction
#### Link to Shiny App: <https://csk01.shinyapps.io/subway/> 
This App was built using R and Shiny. It visaulizes the Chicago CTA/Subway Ridership Data from 2001 to 2021.  

## Data
#### Data Source: <https://data.cityofchicago.org/Transportation/CTA-Ridership-L-Station-Entries-Daily-Totals/5neh-572f>
The data used for this app was downloaded from the Chicago Data Portal website. The original dataset contains 5 columns namely, station-id, station-name, date, day-type and rides spanning from 2001 to 2021. It has 1.09 Million entries.

#### Data preprocessing
Firstly the original data was loaded into a dataframe and then the date was converted to a R friendly format(yyyy-mm-dd) using lubridate library. Then the dataframe was split into 3 dataframes to store as 3 separate data files containing the date and rides columns for OHare Airport, UIC-Halstead and Addison-North Main Stations only. This was done to save space and focus only on the data which I wanted to visualize.  
 
## Source Code
#### Github Repo: <https://github.com/csk01/cta_subway>
Download the repository from Github as a zip file. Extract it into any folder. Open the R code on R studio. You can run it either locally or publish it on Shiny apps.
To run this project you need to download the repo form Github as a zip file and extract it. You need to have R-Studio and ShinyApps installed along with the correct dataset from the source mentioned above. 
Ensure that the below of libraries are up to date.
1. shiny
2. shinydashboard 
3. ggplot2
4. lubridate
5. DT
6. scales
7. dplyr

## Interesting Things


### 1. Impact of Covid-19 
![image](https://user-images.githubusercontent.com/90429287/153971447-8a99ad46-bf23-4a35-a9bd-46d6ffa91260.png)
We can see a sharp decline in number of riders at UIC-Halstead stop after WHO declares Covid-19 a pandemic in March 2020.







