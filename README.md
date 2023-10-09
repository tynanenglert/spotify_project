# spotify_project
An analysis of my lifetime Spotify streaming history including regression, Kmeans clustering, and time series analysis.

## Table of Contents

- Data Sources
- Getting Started
- Data Analysis
- Results


## Data Sources

Spotify listening data was sourced directly from Spotify.  
Geographic data was sourced from IPApi (https://ipapi.co/)

## Getting Started

I started this process by requesting my lifetime streaming history directly from Spotify.  This came after about a week, and was in the format of 11 JSON files.  I inspected the files to ensure that all of the fields were consistent across files and loaded them into a combined data set.  From there, I used the IP address information in the data to obtain location information using IPApi.  I took the geographic information for each IP address and added it to my data set to have a geographic element.  

Once the data was consolidated, I did completed cleaning and consistency checks to identify any duplicate or missing values.  I noticed that the stock "skipped" category had a large number of null values, so I created a new column to measure skipped status based on the existing "reason_end" column.  

I looked at song listening frequency to group songs based on how frequently they appeared in the data.

## Data Analysis 

With the cleaned data, I aggregated total tracks and minutes listened into weekly figures.  I performed a regression analysis on those two variables, and confirmed that they were correlated.  Having a medium-high R2 score (range of 0.6-0.75), I wanted to compare them against each other categorically to identify distinctions of each cluster. 

The comparisons can be found in the Tableau story linked in the results section. 

## Results

The clustering comparison used the measures of total track time and minutes per track for each cluster.  These measures were picked to illustrate overall consumption and concentration of consumption.  I compared each cluster across shuffle tag, skipped tag, and frequency tag.  I ultimately described the qualities of each group based on the distinctions uncovered during the comparisons.  

https://public.tableau.com/shared/3DHNS4QCN?:display_count=n&:origin=viz_share_link)https://public.tableau.com/shared/3DHNS4QCN?:display_count=n&:origin=viz_share_link
