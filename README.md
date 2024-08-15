# Weathering Event Planning, NSS Capstone 

## Data Question

Based upon the past 50 years of weather data, what day(s) have the most consistent weather to plan an outdoor event in Nashville, TN? With this data, a date range(s) (7 days) will be chosen per season to inform when might be the best time to plan an outdoor event in 2025.

## Table of Contents

- [Weathering Event Planning](#project-title)
- [Data Question](#data-question)
- [Table of Contents](#table-of-contents)
- [Executive Summary](#executive-summary)
- [Presentation](#presentation)
- [Technologies](#technologies)
- [Usage](#usage)
- [Motivation](#motivation)
- [Development](#development)
- [Challenges](#challenges)
- [Data Sources](#sources)

## Executive Summary
[(Back to top)](#table-of-contents)

"What’s the weather like?” is a question many of us ask every day; it influences what we wear, what we do, and even our mood. Think about how bad weather can turn a sunny day spent swimming bad with a single clap of thunder or that magical feeling of seeing a hint of sunshine after a week of rain. The weather influences our day-to-day life, so of course that influence is magnified for outdoor events, such as festivals or weddings. Using historical weather data and weather prediction models from the National Oceanic and Atmospheric Administration (NOAA), seasonal windows of 7 days will be identified where the weather has historically been ‘ideal’ for an outdoor event. Ideal weather changes per season, for instance, sunny and not raining is perfect for summer but extreme heat and humidity can make it miserable. Identifying the ideal weather per season, narrowing it to a specific window, and then using it to predict those dates for the upcoming year will be the scope of this project.

## Presentation
[(Back to top)](#table-of-contents)

Link to Presentation Slides: https://docs.google.com/presentation/d/15eRJfFJTaePvzXuaNnAYVntRs_9X8r-j/edit?usp=sharing&ouid=115739610776338485375&rtpof=true&sd=true

Links to Dashboards:

- Winter: https://app.powerbi.com/view?r=eyJrIjoiZTdiZTk3OTEtYjg4Yi00ZDRlLTlkY2MtMzVmYzk4YTcwOWI5IiwidCI6IjEwMWRhNTg3LTE4NDMtNGY1Mi04YjhhLTE3YjA2OWM2NmQzMyIsImMiOjJ9

- Spring: https://app.powerbi.com/view?r=eyJrIjoiZWQ2Y2VhOTctNzZlNy00YTRmLWIwYjQtYjdlNWVkMzRjMzNkIiwidCI6IjEwMWRhNTg3LTE4NDMtNGY1Mi04YjhhLTE3YjA2OWM2NmQzMyIsImMiOjJ9

- Summer: https://app.powerbi.com/view?r=eyJrIjoiZmE2MjA0YWEtODFlYy00ODk0LTlhY2YtNjkzNGViYmRmMDUwIiwidCI6IjEwMWRhNTg3LTE4NDMtNGY1Mi04YjhhLTE3YjA2OWM2NmQzMyIsImMiOjJ9

- Fall: https://app.powerbi.com/view?r=eyJrIjoiNjEwZjdlMWEtMGI2ZC00MDBjLWI5NDYtNDA3Yjk4ZTk5Nzg2IiwidCI6IjEwMWRhNTg3LTE4NDMtNGY1Mi04YjhhLTE3YjA2OWM2NmQzMyIsImMiOjJ9

## Technologies
[(Back to top)](#table-of-contents)

Technologies used:
- Python 3 (Anaconda Jupyter Notebook)

Presentation Components:
- README file (Visual Studio Code) that provides an overview of the project, instructions for 
    running the code, and details on the chosen technologies and techniques.
- Jupyter Notebook
- PowerPoint
- Power BI dashboard for each season to choose dates or date ranges to see the corresponding 
    weather and scores.

## Usage
[(Back to top)](#table-of-contents)

A user can choose a date or date range to see it's daily averages amd score rating, based upon the past 50 years of weather data from the observation station at Nashville International Airport. They can then use this to inform when to plan an outdoor event if that date has 'ideal' historical weather. This project can be replicated for another location if the weather data is available for said location from NOAA.   

## Motivation
[(Back to top)](#table-of-contents)

Outdoor events are very popular across Nashville, TN. From personal family reunions and weddings to corporate sponsored retreats, concerts, or city-wide events like music festivals or marathons, the success and execution of these outdoor events depends greatly upon the weather. Poor weather can lead to decreased attendance, unexpected costs for moving or postponing, or even cancellation of the event. As an event planner, I have personal experience with challenges caused by weather, and predicting when poor weather is least likely to occur will help ensure events are planned accordingly, minimizing the risk of weather-related issues on the execution of the event.

## Development
[(Back to top)](#table-of-contents)

- Download GHCN-Daily report from NOAA National Climatic Data Center for desired observation 
    station (Nashville International Airport).
- Clean data: 
    - Drop any unnecessary columns.
    - Reduce data to prefered time frame.
    - Convert data types where necessary.
    - Create any needed new columns, such as month and day of month.
    - Convert weather variable units where needed (Ex. Celsius to Fahrenheit).
    - Subdivide data set into seasons (Winter: Dec., Jan., Feb.; Spring: Mar., Apr., May; 
        Summer: Jun., Jul., Aug.; Fall: Sep., Oct., Nov.).
- Normalize Data 
    -Each variable was normalized by using the standard deviation to get their z-score.
- Define preferred weather per season for an outdoor event based on seasonal averages and    
    most common weather patterns.
    - Each day was scored based on multiple weather variables, such as precipitation, minimum 
        daily temperature, and average daily wind speed. The z-scores were input into 3 different functions, each given different weights or ranges to the particular weather variables. Each date will then have 3 scores (out of 10) that users can choose from based on their individual weather preferences. For instance, Score 1 may be a 4.5 with all weather variables taken into equal account, but Score 3 might be a 7, making the day more ideal for an outdoor event, taking in a greater chance of cooler temperatures and precipitation.
    - Group each seasonal dataframe by day.
- Determine the 7 day period per season that is most likely to have 'ideal' weather type for 
    each score, using a rolling window aggregate. 
- Use NWS Climate Prediction for Dec. 2024-Nov. 2025 to inform how this date range may be 
    above, below, or on average for temperature and precipitation levels for the upcoming year’s seasons.
 

## Challenges
[(Back to top)](#table-of-contents)

- Data cleaning time can be reduced if user chooses specific time frame, weather variables, 
    and unit preferences when downloading orignal data from NOAA.
- When integrating the data into PowerBI the ungrouped data should be used. Once in PowerBI, 
    the data can then be grouped by day and aggregated to get variable and score averages, minimums, and maximums.
- When grouping by day in PowerBI, the original date column must be split into day and month, 
    even if it was already split in Python. Otherwise, PowerBI won't recognize it as a 'date type'. 

## Data Sources
[(Back to top)](#table-of-contents)

Menne, Matthew J., Imke Durre, Bryant Korzeniewski, Shelley McNeill, Kristy Thomas, Xungang Yin, Steven Anthony, Ron Ray, Russell S. Vose, Byron E.Gleason, and Tamara G. Houston (2012): Global Historical Climatology Network - Daily (GHCN-Daily), Version 3. NOAA National Climatic Data Center. doi:10.7289/V5D21VHZ [31 July 2024]. (https://www.ncei.noaa.gov/metadata/geoportal/rest/metadata/item/gov.noaa.ncdc:C00861/html).

NOAA: National Weather Service’s Climate Prediction Center. (https://www.cpc.ncep.noaa.gov/products/predictions/90day/).




 
