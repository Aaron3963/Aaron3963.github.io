---
title: Library Occupancy Analysis with Weather
weight: 10
summary: A data science project aimed to discover trend of occupancy in Geisel and  WongAvery Library of UCSD. Also tries to answer the question of weather's influence on people's will of coming to libraries.
tags:
  - Data Science
  - Data visualization
  - Pandas
  - Seaborn 
date: '2023-12-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Cover of our presentation
  focal_point: Smart

links:
  - name: Full Project
    url: https://aaron3963.github.io/COGS-108-Project/

url_code: 'https://github.com/Aaron3963/COGS-108-Project'
# url_pdf: 
# url_slides:
url_video: 'https://youtu.be/s202-BIAFj8'
---

{{% callout note %}}
This project is fully rendered online that can be found [here](https://aaron3963.github.io/COGS-108-Project/).
{{% /callout %}}

In this project, we investigated whether weather conditions influence student occupancy patterns at UCSD libraries, specifically Geisel and WongAvery. We combined hourly gate count data from the libraries with weather data from NOAA's La Jolla station, covering the 2022-2023 academic year. After extensive data cleaning to remove outliers, weekends, and nighttime hours, we merged both datasets for analysis.

Our exploratory analysis revealed interesting patterns: Geisel occupancy remained relatively stable throughout quarters, with no dramatic spike during finals week—contrary to common belief. We also found that Fridays and weekends consistently had lower foot traffic. When examining the relationship between temperature and library visits, we observed a weak but positive linear correlation during Fall and Spring quarters, suggesting that milder weather encourages more students to visit. However, Winter quarter showed no clear relationship, as students appeared to visit regardless of temperature.

Overall, while we found some evidence supporting our hypothesis that weather affects library occupancy, the relationship is modest. Many other factors—such as academic schedules, midterms, and personal study habits—likely play more significant roles. We also identified data quality issues with WongAvery and excluded it from final analysis, highlighting the importance of robust data collection for future work.