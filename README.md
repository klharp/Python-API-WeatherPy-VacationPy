# Python API - What's the Weather Like?

## Project Overview
This project used Python scripting to visualize the weather of 500+ world cities at varying distances from the equator. Project focuses on using APIs to visualize weather across the world.

Languages and libraries used:

* Pandas
* Numpy
* Matplotlib
* SciPy
* Time
* OpenWeatherMap API
* Google Places API

If duplicating/running the Jupyter Notebook for this project, an OpenWeather and Google Place API key will be required and entered in the appropriate config.js file.

---

## Analysis Summary
This analysis was performed in February 2021. Data and results will reflect the analysis being performed at this particular time of year.

When analyzing the world-wide weather:

  * There are more representative cities in the northern hemisphere, due to the northern hemisphere having more landmass.
  
  * Temperatures are the warmest in the cities closest to the equator, with the southern hemisphere being warmer than the northern hemisphere. 

  * The northern hemisphere tends to be more humid than the southern.
  
  * There is generally no relationship for locations compared with cloud cover (cloudiness) and wind speed. This is verified in the regression analyses.

 When analyzing the world-wide weather of the 15 cities that met the weather specifications:

 * There are more ideal cities in the northern hempisphere, most of which are a coastal city or located on an island.

 <img src="Images/hotellocations.png" alt="Hotel Locations">

 * My choice for a vacation spot would be the Abaco Beach Resort, in Marsh Harbour, the Bahamas.  
 
  <img src="Images/resort.png" alt="Abaco Beach Resort">

<br />
<br />

  (Image exports are located in the folder titled, Images and csv exports are located in the folder titled, Resources.)

<br />
<br />

# Part I - WeatherPy
## Overview
A Python script was used to visualize the weather of 500+ randomly chosen cities across the world, at varying distances from the equator. Starter code with a [simple Python library](https://pypi.python.org/pypi/citipy) and the [OpenWeatherMap API](https://openweathermap.org/api) was provided.

* Out of the 625 randomly chosen cities, only 576 were used in the analysis. The remaining were eliminated due to incomplete data.

## Scatter plots to show relationships

<img src="Images/LatTemp.png" alt="Temp vs Latitude">
Temperature vs. Latitude is generally showing that the maximum temperatures are the highest closest to the equator (latitude 0). The farther north, the maximum temperatures get colder.

<img src="Images/LatHum.png" alt="Humidity vs Latitude">
Humidity vs. Latitude is generally showing that humidity levels (100% or less) greatly vary across the globe, though higher humidity levels are the majority (greater than 60%), especially in the latitudes between 30 and 70. The northern hemisphere tends to be more humid than the southern.

<img src="Images/LatCloud.png" alt="Cloud Cover vs Latitude">
Cloud Cover (cloudiness) vs. Latitude is generally showing no relationship between cloud cover and location. A majority of the cities are at the extremes, with either very little cloud cover or complete/nearing complete cloud cover.

<img src="Images/LatWind.png" alt="Wind Speed vs Latitude">
Wind Speed  vs. Latitude is generally showing no relationship between wind speed and location.

<br />
<br />

Linear regressions on each relationship for the northern and summer hemispheres were performed. The northern hemisphere was defined as greater than or equal to 0 degrees latitude, and southern hemisphere was defined as less than 0 degrees latitude.

<img src="Images/NTemp.png" alt="Northern Hemispere Temperature vs Latitude">
Northern Hemisphere: Temperature vs. Latitude regression is showing the closer to the equator the warmer the temperature. The r-squared value of 0.78, this is the highest of the coefficients of determination (closest to 1).

<img src="Images/STemp.png" alt="Southern Hemispere Temperature vs Latitude">
Southern Hemisphere: Temperature vs. Latitude regression is not showing as strong of a relationship between temperature and location as in the northern hemisphere. The r-squared value is 0.35.

<img src="Images/NHum.png" alt="Northern Hemispere Humidity vs Latitude">
Northern Hemisphere: Humidity vs. Latitude regression is not showing a strong relationship between location and humidity levels, though the higher latitudes tend to be more humid. The r-squared value is 0.10.

<img src="Images/SHum.png" alt="Southern Hemispere Humidity vs Latitude">
Southern Hemisphere: Humidity vs. Latitude regression, like for the northern hemisphere, is not showing a strong relationship. The r-squared value is 0.02.

<img src="Images/NCloud.png" alt="Northern Hemispere Cloud Cover vs Latitude">
Northern Hemisphere: Cloud Cover (cloudiness) vs. Latitude regression is not showing a strong relationship between location and cloud cover. The r-squared value is 0.03.

<img src="Images/SCloud.png" alt="Southern Hemispere Cloud Cover vs Latitude">
Southern Hemisphere: Cloud Cover (cloudiness) vs. Latitude regression is not showing a strong relationship between location and cloud cover. The r-squared value is 0.13.

<img src="Images/NWind.png" alt="Northern Hemispere Wind Speed vs Latitude">
Northern Hemisphere: Wind Speed vs. Latitude regression is not showing a strong relationship between location and wind speed. The r-squared value is 0.008.

<img src="Images/SWind.png" alt="Southern Hemispere Wind Speed vs Latitude">
Southern Hemisphere: Wind Speed vs. Latitude regression is not showing a strong relationship between location and wind speed. The r-squared value is 0.038.

<br />
<br />

# Part II - VacationPy

## Overview
With the data from Part I, the ideal vacation locations were determined using the [Google Places API](https://developers.google.com/places/web-service/overview).

A heat map was generated for the 585 cities. 

<img src="Images/cities.png" alt="Heat Map of Sample Cities">

The data was reduced to include these ideal conditions:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloud cover (cloudiness).

With these conditions, the first hotel within 5000 meters was located for each of the 15 cities.

<img src="Images/hotellocations.png" alt="Hotel Locations">

