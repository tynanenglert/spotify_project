# spotify_project
An analysis of my lifetime Spotify streaming history including regression analysis, Choropleth map and Kmeans clustering.

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Data Sources](#data-sources)
- [Data Preprocessing](#data-preprocessing)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Data Sources

Spotify listening data was sourced directly from Spotify.  
Geographic data was sourced from IPApi (https://ipapi.co/)

## Getting Started

I started this process by requesting my lifetime streaming history directly from Spotify.  This came after about a week, and was in the format of 10 JSON files.  I inspected the files to ensure that all of the fields were consistent across files and loaded them into a combined data set.  From there, I used the IP address information in the data to obtain location information using IPApi.  I took the geographic information for each IP address and added it to my data set to have a geographic element.  

Once the data was consolidated, I did completed cleaning and consistency checks to identify any problem areas in the data.  I noticed that the stock "skipped" category was lacking, so I created a new column to measure skipped status based on the existing "reason_end" column.  

I also looked at song listening frequency to group songs based on how frequently they appeared in the data.  

## Data Analysis 

With the cleaned data, I aggregated total tracks and minutes listened into weekly figures.  I analyzed the relationship between those two variables using regression, and created categories with Kmeans clustering.  

Taking those clusters, I compared them in Tableau across shuffle tag, skipped tag, and listening frequency tags.  From those comparisons, I was able to identify four groups deterimined by their prevalence in each of those categories for both total tracks played and minutes per track.  

## Results

Present the results of your data analysis. Use tables, charts, or any other appropriate visual aids to convey your findings.


