# Python API Requests & JSON Traversals Visualizing the Weather of 500+ World Cities
![Alt Tag](https://github.com/PetraLee2019/Weatherpy/blob/master/Images/Four%20Seasons.jpg?raw=true)
## Background 
Python script to visualize the weather of 500+ cities across the world of varying distance from the equator using the ![CityPy Python Library](https://pypi.org/project/citipy/), and the ![OpenWeatherMap API](https://openweathermap.org/api).

## Objectives
#### Convert Raw Data to DataFrame

![Alt Tag](https://github.com/PetraLee2019/Weatherpy/blob/master/Images/Merged-Dataframe_Dataset.png?raw=true)

#### Build a series of Scatter Plots to showcase the following relationships:
#### Temperature (F) vs. Latitude
![Alt Tag](https://github.com/PetraLee2019/Weatherpy/blob/master/Images/Max_Temp.png?raw=true)
#### Humidity (%) vs. Latitude
![Alt Tag](https://github.com/PetraLee2019/Weatherpy/blob/master/Images/Humidity.png?raw=true)
#### Cloudiness (%) vs. Latitude
![Alt Tag](https://github.com/PetraLee2019/Weatherpy/blob/master/Images/Cloudiness.png?raw=true)
#### Wind Speed (mph) vs. Latitude
![Alt Tag](https://github.com/PetraLee2019/Weatherpy/blob/master/Images/Wind_Speed.png?raw=true)
- Randomly select at least 500 unique (non-repeat) cities based on latitude and longitude
- Perform a weather check on each of the cities using a series of successive API calls
- Include a print log of each city as it's being processed with the city number and city name
- Save both a CSV of all data retrieved and PNG images for each scatter plot

## Observable Trends
- After collecting weather data from 559 random and diverse cities around the world using the OpenWeatherMap API, which was collected on February 1, 2019, the data illustrated maximum temperature (in Fahrenheit), humidity (%), cloudiness (%) and wind speed (in mph) with the corresponding city, and with respect to the geo-coordinate, Latitude. Expectedly, temperatures are higher closer to the Equator (at 0° Latitude) and are much lower in the Northern Hemishpere, at this time of year in February. It is also of worth to note that temperatures peak at around -20° to -30° Latitude, and drop slightly further into the Southern Hemisphere (at -40° Latitude and below), near the South Pole. This data on temperature is the result of seasons and the tilt of the Earth's axis compared to the plane of its revolution around the Sun. Throughout the year the northern and southern hemispheres are alternately turned either toward or away from the sun depending on Earth's position in its orbit. The hemisphere turned toward the sun receives more sunlight and is in summer, while the other hemisphere receives less sun and is in winter.

- There seems to be little to no correlation between humidity and Latitude as well as with cloudiness and Latitude. The scatter plot visualizations display a considerable amount of heterogeneity even at similar Latitudes. Basically, they're all over the map. However, a small grouping of cities exhibited abnormally low humity levels (at 0% humidity) in the Northern Hemisphere at around 60° to 75° Latitude.

## Considerations
- Be aware of the cities that are used in the query pool. Are you getting coverage of the full gamut of latitudes and longitudes? Or are you simply choosing 500 cities concentrated in one region of the world? Simply rattling 500 cities based on your human selection would create a biased dataset. Be thinking of how this should be countered. (Hint: Consider the full range of latitudes).
- The city data is generated based on random coordinates; as such, the outputs will not be an exact match each time the code is run
- Where and Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before a line of code is written, you should be aiming to have a crystal clear understanding of your intended outcome
