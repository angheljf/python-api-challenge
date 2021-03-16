# Python API Homework - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

## Part I - WeatherPy

![Weather](Images/weather.png)

In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

The first requirement is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude

![Weather](Images/Latitude_Temperature.png)

* Humidity (%) vs. Latitude

![Weather](Images/Latitude_Humidity.png)

* Cloudiness (%) vs. Latitude

![Weather](Images/Latitude_Cloudiness.png)

* Wind Speed (mph) vs. Latitude

![Weather](Images/Latitude_WindSpeed.png)

After each plot, add a sentence or two explaining what the code is analyzing.

The second requirement is to run linear regression on each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude

![Weather](Images/NH_temp_vs_lat.png)

* Southern Hemisphere - Temperature (F) vs. Latitude

![Weather](Images/SH_temp_vs_lat.png)

* Northern Hemisphere - Humidity (%) vs. Latitude

![Weather](Images/NH_hum_vs_lat.png)

* Southern Hemisphere - Humidity (%) vs. Latitude

![Weather](Images/SH_hum_vs_lat.png)

* Northern Hemisphere - Cloudiness (%) vs. Latitude

![Weather](Images/NH_cloud_vs_lat.png)

* Southern Hemisphere - Cloudiness (%) vs. Latitude

![Weather](Images/SH_cloud_vs_lat.png)

* Northern Hemisphere - Wind Speed (mph) vs. Latitude

![Weather](Images/NH_speed_vs_lat.png)

* Southern Hemisphere - Wind Speed (mph) vs. Latitude

![Weather](Images/SH_speed_vs_lat.png)

After each pair of plots, take the time to explain what the linear regression is modeling. For example, describe any relationships you notice and any other analysis you may have.

Your final notebook must:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

![Vacation](Images/vacation.png)

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

* **Note:** Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure you can't be charged. Check out [Google Maps Platform Billing](https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption) and [Manage your cost of use](https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps) for more information.

* **Note:** if you having trouble displaying the maps, try running `jupyter nbextension enable --py gmaps` in your environment and retry.

To complete this part of the assignment,you will need to do the following:

* Create a heat map that displays the humidity for every city from Part I.

![Vacation](Images/heatmap.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

![Vacation](Images/heatmapwithmarkers.png)

As final considerations:

* You must complete your analysis using a Jupyter notebook.
* You must use the Matplotlib or Pandas plotting libraries.
* For Part I, you must include a written description of three observable trends based on the data.
* For Part II, you must include a screenshot of the heatmap you create and include it in your submission.
* You must use proper labeling of your plots, including aspects like: Plot Titles (with date of analysis) and Axes Labels.
* For max intensity in the heat map, try setting it to the highest humidity found in the data set.
