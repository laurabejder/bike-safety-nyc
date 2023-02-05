# Bike safety in New York City

This is my first project data studios. The promp for this project was 'something you miss from home' and as a Dane, my mind went straight to biking. I was curious to how dangerous it is to bike in New York City and how it compares to my home town Copenhagen.

## In this repository
### Notebooks
- `accidents_data_cleaning.ipynb`: This notebook cleans the dataset [Motor Vehicle Collisions - Crashes](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95) from the [NYC Open Data](https://opendata.cityofnewyork.us/) portal. The dataset contains information on all crashes but for this project I am only interested in crashes involving bikes. The main part of the cleaning is thus to sorting the dataset to only include bike accidents.
- `accidents_data_visualization.ipynb`: In this notebook I prepare the data from the csv `nyc_bike_accidents.csv` for data visualization.
- `nyc_cph_comparison.ipynb`: This notebook contains some comparison of the bike safety in New York and Copenhagen. 

### Inside the `data` directory:
- `cph_bike_accidents.csv`: Accidents in Copenhagen 2012-2022.
- `cph_population.csv`: Number of population in Copenhagen
- `nyc_accidents_development_2012_2021.csv`: Injury rate and fatality rate per 1 million biker in New York 2012-2021.
- `nyc_accidents_development_2012_2021_long.csv`: Long version of `nyc_accidents_development_2012_2021.csv` (used for visualization)
- `nyc_accidents_reason_5.csv`: Top five reasons for bike accidents in 2022 (used for visualization)
- `nyc_bike_accidents_2018_2022.csv`: Location and outcome of each accident from 2018-2022.
- `nyc_bike_accidents.csv`: Complete data on all bike accidents
- `nyc_bike_accidents_2022`: Data on all bike accidents in 2022
- `nyc_bikerides_numbers.csv`: Estimated number of daily bike rides in NYC 2008-2021
- `nyc_injuries_development_2012_2021.csv`: Total number of bike accident injuries 2012-2022
- `shape_files` directory: Shapefiles of the bike lanes in NYC from 2017-2022.

## Project description

### Aim of the project
This project examines the bike safety and the condition of the bike infrastructure in New York City. It looks into the location and reasons for accidents that result in the injury or death of a cyclist and visually illustrate how the city has tried to improve bike safety by expanding its network of protected bike lanes.

### Findings
I found that bike accidents in 2022 were clustered around Lower Manhattan and Brooklyn. The most common causes for bike accidents were inattentive or distracted car drivers or cars that failed to yield right-of-way.

By mapping the shapefiles of the protected bike lanes over time, it became clear that New York City has expanded its bike infrastructure, but that large areas of the city are scarcely covered by protected bike lanes. When I plottet the fatal accidents on top of the protected bike lanes, it also showed that many of the fatal accidents happen where there are no protected bike lanes.  

Lastly I standardized the number of yearly accidents by number of bike rides (accidents per 1 million) which showed that it has become a little safer to bike in New York. 

### Data collection
This project uses a patchwork of data to examine bike safety in New York. Most of the New York data comes from NYC Open data:

- Bike accidents in NYC: [NYC Open Data, Motor Vehicle Collisions - Crashes](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)
- NYC bike lanes: [NYC Open Data, New York City Bike Routes](https://data.cityofnewyork.us/Transportation/New-York-City-Bike-Routes/7vsa-caz7#revert)
- Shape files of NYC: [The University of Texas at Austin, GeoData](https://geodata.lib.utexas.edu/?f%5Bdc_format_s%5D%5B%5D=Shapefile&f%5Bdct_spatial_sm%5D%5B%5D=New+York%2C+New+York%2C+United+States&per_page=50)
- Number of bike riders in NYC: [NYC DOT Cycling in the City](https://www.nyc.gov/html/dot/html/bicyclists/cyclinginthecity.shtml)

This repository also contains data on bike accidents in Copenhagen. This data isn't included in the article because it wasn't possible to properly standardize it by number of bike riders and thus make it comparable to New York City.
- Bike accidents in Copenhagen: [Statistics Denmark, Traffic Accidents](https://www.statistikbanken.dk/20056)

### Data analysis process
I started out with a dataset of all Motor Vehicle Collisions in New York City from 2012 to 2023. Despite the name, this dataset also includes solo bike accidents (crashes where only one bike and no other vehicles were involved). 

I cleaned the dataset so it only includes accidents where a bike was involved. When I had the bike accident dataset, I started looking into the location of and the reasons for the accidents. Looking at the locations involved plotting the data to get a better sense of how they were spread geographically. For the accidents I looked at the given reason and split it up by whether the reason was caused by a bike or not.

For the lane analysis, I had to plot the data in QGIS to properly see how the bike lanes have changed over time. I decided only to include category I (protected) bike lanes in my mapping. All other types were excluded.

On top of the protected bike lanes in 2022, I plottet all the fatal accidents to get a better sense of whether there seem to be a pattern between protected bike lanes and fatal accidents. Unlike accidents resulting in injuries, fatal accidents are scatteret all across the city, many of them in areas without protected bike lanes. However, thankfully there aren’t many fatal bike accidents each year, so it is difficult to say anything conclusive about a potential relationship between bike lanes and deaths.

### New skills
I spent quite a bit of time in QGIS mapping New York, bikelanes, accidents etc. and making all the information comprehensible to a reader. And I now feel more confident working with QGIS to make maps that are beyond the limits of datawrapper. 

In this project I also managed to create a simple javascript function that makes a series of images shift between each other. This allowed me to better illustrate how the bike lane network has been expanded over time. I enjoyed having a visual idea and actually be able to create it (although the quality could have been better – time to learn illustrator?) and expanding these skills is definitely something I'll work on during the next projects. 

Another thing I have learned while working on this project, is how difficult it can be to make comparisons. I began with an idea of comparing number of bike accidents in Copenhagen and New York. However, for this number to make any sense, it had to be put in relation to the number of people who actually bike in each city. It turned out to be impossible to get reliable numbers for Copenhagen. I could have standardized by population but I know from experience  and research that a much larger share of Copenhageners bike so those numbers would have been pretty off. Unable to standardize and then compare the accident numbers, I had to pivot and focus more on New York City in itself. Going through those though processes has made me more aware of the limitations of data.

### Further work
If I had more time (or more skills) I would have liked to build on the comparison between Copenhagen and New York. I would either need to get access to additional data or find a way to properly standardize the numbers I have now. 

I would also like to add to the visual side of the article. I have had a hard time finding a picture or video that could serve as an appetizer in the beginning of the article. 

At last, I would like to expand on the analysis of the relationship between protected bike lanes and fatal bike accidents. I reached a point where I could point to a weak indication of a relationship but I would need more data and time to be able to say anything more conclusive. For now it could be a signal but it could also be noise. 
