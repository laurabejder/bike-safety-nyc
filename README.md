# Bike safety in New York City

This is my first project data studios. The promp for this project was 'something you miss from home' and as a Dane, my mind went straight to biking. I was curious to how dangerous it is to bike in New York City and how it compares to my home town Copenhagen.

## Aim of the project
This project examines the bike safety and the condition of the bike infrastructure in New York City. It looks into the location and reasons for accidents that result in the injury or death of a cyclist and visually illustrate how the city has tried to improve bike safety by expanding its network of protected bike lanes.

## Findings
I found that bike accidents are clustered around Lower Manhattan and Brooklyn

Most common causes for accidents ... 

By mapping the shapefiles of the protected bike lanes over time, it became clear that the .... 

Standardized the number of accidents by number of bike rides, accidents per 1 million, it has become a little safer to bike in New York. 


## Data collection
- Summary of the data collection process, with links

- Bike accidents in NYC: [NYC Open Data, Motor Vehicle Collisions - Crashes](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)
- NYC bike lanes: [NYC Open Data, New York City Bike Routes](https://data.cityofnewyork.us/Transportation/New-York-City-Bike-Routes/7vsa-caz7#revert)
- Shape files of NYC: [The University of Texas at Austin, GeoData](https://geodata.lib.utexas.edu/?f%5Bdc_format_s%5D%5B%5D=Shapefile&f%5Bdct_spatial_sm%5D%5B%5D=New+York%2C+New+York%2C+United+States&per_page=50)
- Number of bike riders in NYC: [NYC DOT Cycling in the City](https://www.nyc.gov/html/dot/html/bicyclists/cyclinginthecity.shtml)

This repository also contains data on bike accidents in Copenhagen. This data isn't included in the article because it wasn't possible to properly standardize it by number of bike riders and thus make it comparable to New York City.
- Bike accidents in Copenhagen: [Statistics Denmark, Traffic Accidents](https://www.statistikbanken.dk/20056)

## Data analysis process
Got dataset of all Motor Vehicle Collisions in New York City from 2012 to 2023.
despite the name, this dataset also includes solo bike accidents (crashes where only one bike and no other vehicles were involved). 

## New skills
I spent quite a bit of time in QGIS mapping New York, bikelanes, accidents etc. and making all the information comprehensible to a reader. And I now feel more confident working with QGIS to make maps that are beyond the limits of datawrapper. 

In this project I also managed to create a simple javascript function that makes a series of images shift between each other. This allowed me to better illustrate how the bike lane network has been expanded over time. I enjoyed having a visual idea and actually be able to create it (although the quality could have been better – time to learn illustrator?) and expanding these skills is definitely something I'll work on during the next projects. 

Another thing I have learned while working on this project, is how difficult it can be to make comparisons. I began with an idea of comparing number of bike accidents in Copenhagen and New York. However, for this number to make any sense, it had to be put in relation to the number of people who actually bike in each city. It turned out to be impossible to get reliable numbers for Copenhagen. I could have standardized by population but I know from experience  and research that a much larger share of Copenhageners bike so those numbers would have been pretty off. Unable to standardize and then compare the accident numbers, I had to pivot and focus more on New York City in itself. Going through those though processes has made me more aware of the limitations of data.

## Further work
- A section about things you tried to do or wanted to do but did not have the skills/time (but if you have more time you might do)

