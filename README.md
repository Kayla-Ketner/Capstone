# Weathering Event Planning, NSS Capstone 

# Data Question

Based upon the past 50 years of weather data, what day(s) have the most consistent weather to plan an outdoor event in Nashville, TN? With this data, a date range(s) (7 days) will be chosen per season for 2025 to plan an outdoor event.

# Table of Contents

- [Weathering Event Planning](#project-title)
- [Data Question](#data-question)
- [Table of Contents](#table-of-contents)
- [Executive Summary](#executive-summary)
- [Usage](#usage)
- [Development](#development)
- [Challenges](#challenges)
- [Data Sources](#sources)

# Executive Summary
[(Back to top)](#table-of-contents)

‘What’s the weather like?” is a question many of us ask every day; it influences what we wear, what we do, and even our mood. Think about how bad weather can turn a great day bad with a single clap of thunder, or that magical feeling of seeing a hint of sunshine after a week of rain. The weather influences our day-to-day life, so of course that influence is magnified for outdoor events, such as festivals or weddings. Using historical weather data and weather prediction models from the National Oceanic and Atmospheric Administration (NOAA), I will identify seasonal windows of 7-14 days where the weather has historically been ‘ideal’ for an outdoor event. Ideal weather changes per season, for instance, sunny and not raining is perfect for summer but extreme heat and humidity can make it miserable. Identifying the ideal weather per season, narrowing it to a specific window, and then using it to predict those dates for the upcoming year will be the scope of this project. The data is readily available; however, cleaning it will be the primary challenge.

# Usage
[(Back to top)](#table-of-contents)

Motivation
Outdoor events are very popular across Nashville, TN. From personal family reunions and weddings to corporate sponsored retreats, concerts, or city-wide events like music festivals or marathons, the success and execution of these outdoor events depends greatly upon the weather. Poor weather can lead to decreased attendance, unexpected costs for moving or postponing, or even cancellation of the event. As an event planner, I have personal experience with challenges caused by weather, and predicting when poor weather is least likely to occur will help ensure events are planned accordingly, minimizing the risk of weather-related issues on the execution of the event

# Development
[(Back to top)](#table-of-contents)

# Challenges
[(Back to top)](#table-of-contents)

Explain any anticipated challenges with your project, and your plan for managing them:
●	Data Cleaning, including narrowing to the information actually needed for scope of project and making sure it is listed in the appropriate data type
●	Integrating the cleaned data into a Tableau or PowerBI dashboard without having to re-clean it completely
○	Maybe do majority of cleaning in Excel? But just for weather predication data?

# Data Sources
[(Back to top)](#table-of-contents)

Menne, Matthew J., Imke Durre, Bryant Korzeniewski, Shelley McNeill, Kristy Thomas, Xungang Yin, Steven Anthony, Ron Ray, Russell S. Vose, Byron E.Gleason, and Tamara G. Houston (2012): Global Historical Climatology Network - Daily (GHCN-Daily), Version 3. NOAA National Climatic Data Center. doi:10.7289/V5D21VHZ [31 July 2024]. (https://www.ncei.noaa.gov/metadata/geoportal/rest/metadata/item/gov.noaa.ncdc:C00861/html).

NOAA: National Weather Service’s Climate Prediction Center. (https://www.cpc.ncep.noaa.gov/products/predictions/90day/).



Minimum Viable Product (MVP)
Define your MVP. This should be a description of what your final capstone will look like, including visualizations, how the analysis will be presented, who the intended audience is, etc.:
•	Audience: Anyone wanting to plan an outdoor event in Nashville, TN. An outdoor event is going to be defined as a gathering of 100 people or more.
•	Data Analysis
o	Define preferred weather per season (Winter: Dec., Jan., Feb.; Spring: Mar., Apr., May; Summer: Jun., Jul., Aug.; Fall: Sep., Oct., Nov.) for an outdoor event based on seasonal averages and most common weather patterns
o	Determine the 7-14 day period per season that is most likely to have that weather type 
o	Use NWS Climate Prediction for Dec. 2024-Nov. 2025 to choose that period for the upcoming year’s season
•	Presentation Components
o	A README file that provides an overview of the project, instructions for running the code, and details on the chosen technologies and techniques
o	Notebook visuals and potentially a map visual of some kind on a PPT
o	A dashboard in either Tableau or PowerBI for choosing a particular date range to see its weather or choose a weather pattern to get a date range for it



 
