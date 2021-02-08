# Python API Homework - What's the Weather Like?

# Part I - WeatherPy
## WeatherPy Analysis Summary
This analysis was performed in February 2021, using the OpenWeatherMap API.

  
  * Temperatures are the warmest in the cities closest to the equator, with the southern hemisphere being warmer than the northern hemisphere. This may be due to the northern hemisphere having more landmass.
  * The northern hemisphere tends to be more humid than the southern.
  * There is generally no relationsship location compared with cloud cover (cloudiness) and wind speed. This is verified in the regression analyses.

## Overview
Develop a Python script to visualize the weather of 500+ randomly chosen cities across the world, at varying distances from the equator. Starter code with a [simple Python library](https://pypi.python.org/pypi/citipy) and the [OpenWeatherMap API](https://openweathermap.org/api) was provided.

* Out of the 617 randomly chosen cities, only 579 were used in the analysis. The remaining were eliminated due to incomplete data.

## Scatter plots to show any relationships

<img src="Images/LatTemp.png" alt="Temp vs Latitude">
Temperature vs. Latitude is generally showing that the maximum temperatures are the highest closest to the equator (0). The farther north, the maximum temperatures get colder.

<img src="Images/LatHum.png" alt="Humidity vs Latitude">
Humidity vs. Latitude is generally showing that humidity levels (100% or less) greatly vary across the globe, though higher humidity levels are the majority (greater than 60%). The northern hemisphere tends to be more humid than the southern.

<img src="Images/LatCloud.png" alt="Cloud Cover vs Latitude">
Cloud Cover vs. Latitude (cloudiness) is generally showing no relationship between cloud cover and location.

<img src="Images/LatWind.png" alt="Wind Speed vs Latitude">
Wind Speed  vs. Latitude is generally showing no relationship between wind speed and location.

<br />
<br />

Linear regression on each relationship for the northern and summer hemispheres were performed. The northern hemisphere was defined as greater than or equal to 0 degrees latitude, and southern hemisphere was defined asless than 0 degrees latitude.

<img src="Images/NTemp.png" alt="Northern Hemispere Temperature vs Latitude">
Northern Hemisphere: Temperature vs. Latitude regression is showing the closer to the equator the warmer the temperature. The r-squared value of 0.76, this is the highest of the coefficients of determination (closest to 1).

<img src="Images/STemp.png" alt="Southern Hemispere Temperature vs Latitude">
Southern Hemisphere: Temperature vs. Latitude regression is not showing as strong of a relationship between temperature and location as in the northern hemisphere. The r-squared value is 0.28.

<img src="Images/NHum.png" alt="Northern Hemispere Humidity vs Latitude">
Northern Hemisphere: Humidity vs. Latitude regression is not showing a strong relationship between location and humidity levels. The r-squared value is 0.13.

<img src="Images/SHum.png" alt="Southern Hemispere Humidity vs Latitude">
Southern Hemisphere: Humidity vs. Latitude regression, like for the northern hemisphere, is not showing a strong relationship. The r-squared value is 0.017.

<img src="Images/NCloud.png" alt="Northern Hemispere Cloud Cover vs Latitude">
Northern Hemisphere: Cloud Cover (cloudiness) vs. Latitude regression is not showing a strong relationship between location and cloud cover. The r-squared value is 0.015.

<img src="Images/SCloud.png" alt="Southern Hemispere Cloud Cover vs Latitude">
Southern Hemisphere: Cloud Cover (cloudiness) vs. Latitude regression is not showing a strong relationship between location and cloud cover. The r-squared value is 0.087.

<img src="Images/NWind.png" alt="Northern Hemispere Wind Speed vs Latitude">
Northern Hemisphere: Wind Speed vs. Latitude regression is not showing a strong relationship between location and wind speed. The r-squared value is 0.015.

<img src="Images/SWind.png" alt="Southern Hemispere Wind Speed vs Latitude">
Southern Hemisphere: Wind Speed vs. Latitude regression is not showing a strong relationship between location and wind speed. The r-squared value is 0.065.

<br />
<br />

# Part II - VacationPy

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

* **Note:** Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure you can't be charged. Check out [Google Maps Platform Billing](https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption) and [Manage your cost of use](https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps) for more information.

To complete this part of the assignment,you will need to do the following:

* Create a heat map that displays the humidity for every city from Part I.

  ![heatmap](Images/heatmap.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number; e.g., 10. 

* Use Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)

As final considerations:

* You must complete your analysis using a Jupyter notebook.
* You must use the Matplotlib or Pandas plotting libraries.
* For Part I, you must include a written description of three observable trends based on the data.
* For Part II, you must include a screenshot of the heatmap you create and include it in your submission.
* You must use proper labeling of your plots, including aspects like: Plot Titles (with date of analysis) and Axis Labels.
* For max intensity in the heat map, try setting it to the highest humidity found in the data set.

## Hints and Considerations

* The city data you generate is based on random coordinates as well as different query times. As such, your outputs will not be an exact match to the provided starter notebook.
Jupyter Notebook
README.md
2 minutes agoJupyter Notebook
README.md
3 minutes ago
GitHub Flavored Markdown
File
Edit
View
Language
1
# Python API Homework - What's the Weather Like?
2
​
3
## Background
4
​
5
Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"
6
​
7
Now, we know what you may be thinking: _"Duh. It gets hotter..."_
8
​
9
But, if pressed, how would you **prove** it?
10
​
11
![Equator](Images/equatorsign.png)
12
​
13
### Before You Begin
14
​
15
1. Create a new repository for this project called `python-api-challenge`. **Do not add this homework to an existing repository**.
16

GitHub Flavored Markdown
File
Edit
View
Language
1
# Python API Homework - What's the Weather Like?
2
​
3
## Background
4
​
5
Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"
6
​
7
Now, we know what you may be thinking: _"Duh. It gets hotter..."_
8
​
9
But, if pressed, how would you **prove** it?
10
​
11
![Equator](Images/equatorsign.png)
12
​
13
### Before You Begin
14
​
15
1. Create a new repository for this project called `python-api-challenge`. **Do not add this homework to an existing repository**.
16

* If you'd like a refresher on the geographic coordinate system, [this site](http://desktop.arcgis.com/en/arcmap/10.3/guide-books/map-projections/about-geographic-coordinate-systems.htm) has great information.

* Next, spend the requisite time necessary to study the OpenWeatherMap API. Based on your initial study, you should be able to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should aim to have a crystal clear understanding of your intended outcome.

* Starter code for Citipy has been provided. However, if you're craving an extra challenge, push yourself to learn how it works by checking out the [citipy Python library](https://pypi.python.org/pypi/citipy). Before you try to incorporate the library into your analysis, start by creating simple test cases outside your main script to confirm that you are using it correctly. Too often, when introduced to a new library, students get bogged down by the most minor of errors -- spending hours investigating their entire code -- when, in fact, a simple and focused test would have shown their basic utilization of the library was wrong from the start. Don't let this be you!

* Part of our expectation in this challenge is that you will use critical thinking skills to understand how and why we're recommending the tools we are. What is Citipy for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?

* In building your script, pay attention to the cities you are using in your query pool. Are you getting coverage of the full gamut of latitudes and longitudes? Or are you simply choosing 500 cities concentrated in one region of the world? Even if you were a geographic genius, simply rattling 500 cities based on your human selection would create a biased dataset. Be thinking of how you should counter this. (Hint: Consider the full range of latitudes).

* Once you have computed the linear regression for one chart, the process will be similar for all others. As a bonus, try to create a function that will create these charts based on different parameters.

* Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.

* Ensure your repository has regular commits (i.e. 20+ commits) and a thorough README.md file.

* Lastly, remember -- this is a challenging activity. Push yourself! If you complete this task, then you can safely say that you've gained a strong mastery of the core foundations of data analytics and it will only go better from here. Good luck!


