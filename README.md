# Python API Challenge - What's the Weather Like?

## Part 1: WeatherPy

### Background
In this section, I created a Python script to visualize the weather of 500+ cities of varying distance from the equator. I accomplished this using Python libraries and the [OpenWeatherMap API](https://openweathermap.org/api).

### Materials
- Python Script: [WeatherPy.ipynb](/WeatherPy/WeatherPy.ipynb)
- Scatter Plots and Linear Regressions images: [outputData](/WeatherPy/outputData)

### Observations
- In the northern hemisphere, as you move away from the equator, the temperature decreases. This is seen by the linear regression plot, which has an r-value of -0.60, indicating a moderate/strong negative correlation.
- In the southern hemisphere, as you get closer to the equator, the temperatures increases. This is seen by the linear regression plot, which has an r-value of 0.78, indicating a moderate/strong positive correlation.
- The correlation between latitude and temperature isn't perfect, as other factors such as elevation, ocean currents, and precipitation also affect climate patterns.
- Based on the other linear regression plots, there is no correlation (r-value < 0.3) between:
    - Latitude and Humidity %
    - Latitude and Cloudiness %
    - Latitude and Wind Speed

### Analysis
The first part of the analysis was to build a series of scatter plots to showcase the following relationships:
- Temperature (F) vs. Latitude
![image](/WeatherPy/outputData/Latitude%20vs%20Max%20Temperature.png)

- Humidity (%) vs. Latitude
![image](/WeatherPy/outputData/Latitude%20vs%20Humidity.png)

- Cloudiness (%) vs. Latitude
![image](/WeatherPy/outputData/Latitude%20vs%20Cloudiness.png)

- Wind Speed (mph) vs. Latitude
![image](/WeatherPy/outputData/Latitude%20vs%20Wind%20Speed.png)

The second part of the analysis was to compute the linear regression for each relationship. This time, I separated the plots into Northern Hemisphere and Southern Hemisphere. 
- Northern Hemisphere - Temperature (F) vs. Latitude
    ![image](/WeatherPy/outputData/NH%20-%20Max%20Temp%20vs%20Latitude%20Regression.png)
    In the northern hemisphere, as you move away from the equator, the temperature decreases (negative correlation).
- Southern Hemisphere - Temperature (F) vs. Latitude
    ![image](/WeatherPy/outputData/SH%20-%20Max%20Temp%20vs%20Latitude%20Regression.png)
    In the southern hemisphere, as you move closer to the equator, the temperature increases (positive correlation).
- Northern Hemisphere - Humidity (%) vs. Latitude
    ![image](/WeatherPy/outputData/NH%20-%20Humidity%20vs%20Latitude%20Regression.png)
    No correlation between the latitude of a city and the percentage of humidity.
- Southern Hemisphere - Humidity (%) vs. Latitude
    ![image](/WeatherPy/outputData/SH%20-%20Humidity%20vs%20Latitude%20Regression.png)
    No correlation between the latitude of a city and the percentage of humidity.
- Northern Hemisphere - Cloudiness (%) vs. Latitude
    ![image](/WeatherPy/outputData/NH%20-%20Cloudiness%20vs%20Latitude%20Regression.png)
    No correlation between the latitude of a city and the percentage of cloudiness.
- Southern Hemisphere - Cloudiness (%) vs. Latitude
    ![image](/WeatherPy/outputData/SH%20-%20Cloudiness%20vs%20Latitude%20Regression.png)
    No correlation between the latitude of a city and the percentage of cloudiness.
- Northern Hemisphere - Wind Speed (mph) vs. Latitude
    ![image](/WeatherPy/outputData/NH%20-%20Wind%20Speed%20vs%20Latitude%20Regression.png)
    No correlation between the latitude of a city and the speed of the wind.
- Southern Hemisphere - Wind Speed (mph) vs. Latitude
    ![image](/WeatherPy/outputData/SH%20-%20Wind%20Speed%20vs%20Latitude%20Regression.png)
    No correlation between the latitude of a city and the speed of the wind.

## Part 2: VacationPy

### Background
In section 2 of the challenge, I used my skills working with weather data to plan future vacations. For this, I used Jupyter-gmaps and the [Google Places API](https://developers.google.com/maps/documentation/places/web-service/overview).

### Materials
- Python Script: [VacationPy.ipynb](/WeatherPy/VacationPy.ipynb)
- Screenshot of Heatmap: [Here](/WeatherPy/outputData/Humidity%20Heatmap%20(VacationPy).png)
- Screenshot of HeatMap with Hotel Markers: [Here](/WeatherPy/outputData/Humidity%20Heatmap%20with%20Hotels%20(VacationPy).png)

### Analysis
In the analysis, I created a heat map that displays the humidity for every city from Part 1, as in the following image:
![image](/WeatherPy/outputData/Humidity%20Heatmap%20(VacationPy).png)

I then narrowed down my data to find cities where all of the following "ideal" conditions were met:
- Max Temp is below 80 but at least 70
- Wind Speed is less than 10 mph
- Cloudiness is 0%
- Humidity is less than 80%

The data resulted in 8 cities: 
- Port Elizabeth (South Africa)
- Cape Town (South Africa)
- Bonito (Brazil)
- Kruisfontein (South Africa)
- Portland (US)
- Cassilândia (Brazil)
- Oudtshoorn (South Africa)
- Union (US)

I then created marker layers over the cities in the map. When you click on a specific marker layer, it will display the name of the city and the closest hotel.
![image](/WeatherPy/outputData/Humidity%20Heatmap%20with%20Hotels%20(VacationPy).png)
