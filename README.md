# Krishnan Chelakkarai Sivaraman |  CS424 - Project-1 - Subway  

## Introduction
#### Link to Shiny App: <https://csk01.shinyapps.io/subway/> 
#### Youtube Video <https://youtu.be/8CBXgb6cLjk>

This App was built using R and Shiny. It visaulizes the Chicago CTA/Subway Ridership Data from 2001 to 2021.  

The landing page is a dashboard to let the user compare the entries at for each year. The first plot compares the entries at UIC-Halstead on the left section and O'Hare on the right section of the page. The user can select the station from the dropdown list to compare the stations(O'Hare, UIC-Halsted and Addison)

![image](https://user-images.githubusercontent.com/90429287/153977671-aad2b0b7-a738-45b1-8039-e1e4817dce4e.png)


The second set of bar plots compare the total entries of a station in a given year based on the type of filter. The user can select the Year from the dropdown menu and the charts update for the chosen year. Likewise the User can choose to compare the data either per day, month or day of the week.
The plots below shows the comparison of daily entries at UIC-Halstead vs O'Hare.

![image](https://user-images.githubusercontent.com/90429287/153977724-c9a6670d-72e7-4e35-911c-2e35e60e4dac.png)


Below is an example where the ridership data is shown monthly on the left and weekly on the right 

![image](https://user-images.githubusercontent.com/90429287/153978232-c27950a8-9f95-437a-bc55-8e9903141f95.png)

Lastly the same data is presented in a tabular form and the User can select the number of entries being displayed

![image](https://user-images.githubusercontent.com/90429287/153978517-68b58c13-27b4-45cd-8747-68fa6bf8ba9d.png)


The user can choose the Interesting Dates option in the sidemenu and navigate to view the visualizations of 10 interesting trends observed in this dataset. The user can select the visualization to view from the date dropdown menu on the bottom of the screen

![image](https://user-images.githubusercontent.com/90429287/153979109-00be925c-49e0-4eba-81f4-3f1633dac54d.png)



  
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
The data showed a lot of trends in CTA ridership over the years. Here are some of the ones which are presented in the application

### 1. Impact of Covid-19 
The most obivious trend was the sharp decline in number of riders at UIC-Halstead stop which was right after WHO declares Covid-19 a pandemic in March 2020.


![image](https://user-images.githubusercontent.com/90429287/153971447-8a99ad46-bf23-4a35-a9bd-46d6ffa91260.png)

### 2. Cubs Game 
Despite dull times during the pandemic we can clearly see a two spikes in ridership at OHare due to the Cubs vs Cardinals Baseball game on Sep 4th and Sep 6th 2020

![image](https://user-images.githubusercontent.com/90429287/153971668-10441a69-cc9d-4c2d-8b8e-0750bff409e9.png)

### 3. 9/11 Aftermath Game 
Another trend was the sudden drop in rider count at the OHare CTA right after the 9/11 World Trade Center Attacks in 2001

![image](https://user-images.githubusercontent.com/90429287/153972326-7e949056-2d94-4ced-8444-b2674e95d60b.png)

### 4. BLM Protest 
Missing data for June can be attributed to sudden halting of services due to protests in the wake of death of George Floyd

![image](https://user-images.githubusercontent.com/90429287/153972569-629c4d1d-a25e-497e-82ec-e8d792d54a77.png)

### 5. 7-Oct-2008 
This day was an eventful day. The sudden spike on in ridership could be attributed to a number of reasons 
1. Obama arriving at OHare to cast his vote
2. First match for the Cubs world series begins
3. Kanye West performing at United center 

![image](https://user-images.githubusercontent.com/90429287/153972819-9bb50318-ad82-4698-95e2-8a471ae3b029.png)

### 6. Winter Break UIC
We dont see the usual number of riders at the UIC-Halstead stop from Dec 15 2018 to Jan 15 2019 due to UIC's Winter Break

![image](https://user-images.githubusercontent.com/90429287/153973056-d0550408-243f-4f55-a691-6608f64bda7b.png)

### 7. Train Derails 
Due to the derailment of a Blue Line at OHare on March 24, the OHare station had little to no riders from March 24 - 30 2014

![image](https://user-images.githubusercontent.com/90429287/153973219-c23c95d8-62f1-41c4-b682-a74099814b2a.png)

### 8. OHare CTA Station Renovation
In 2019, there were no data for brief period from Sep 27 - Oct 06 as Ohare CTA shuts down for renovation for a project

![image](https://user-images.githubusercontent.com/90429287/153973739-fef6df6f-35cf-4966-953e-2a9bb8de130e.png)

### 9. Chicago Cubs victory
Chicago knows how to support its basesball team. We can see an unusual increase in the number of riders because of Chicago Cubs victory parade and rally on 4th Nov. 2016 at UIC

![image](https://user-images.githubusercontent.com/90429287/153973844-6e8e514d-88a5-469f-a16c-9b96895eec61.png)

### 10. Yet another Cubs game
Spike seen in OHare ridership in July 2013 due to Cubs game at Wrigley Field. This tells us that Chicagoans do not mind travelling 10 miles to support the Cubs 

![image](https://user-images.githubusercontent.com/90429287/153974630-4dc60252-99f1-4dbb-8c90-fe1b69db99b7.png)



