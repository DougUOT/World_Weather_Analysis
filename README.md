# World_Weather_Analysis
Using Jupyter Notebook, Pandas Library, CityPy, Python, APIs and JSON Traversals, to get more than 500 random cities around the world in order to show the relationship between Latitude and an assortment of weather parameters

## Overview of Project

Mytrip is a top travel technology company specializing in internet-related services in the hotel and lodging industry.
We will gather and present information for clients through the pursuit page; the customer will filter based on their preferred travel criteria to find their hotel anyplace on the planet. We will utilize a Jupiter notebook and the CityPI module to play out this undertaking to get random cities and latitudes. We will use the Matplotlib to create a series of scatter plots to show the relationship between the latitude and various weather parameters for over 500 cities. This data will help the company to predict the best time of year for customers to plan their vacation

This assignment is related to the Bootcamp Data Analytics from the University of Toronto and comprises the goals below for this module: 

Follow below the goals for this module:

1) Objective 1: Retrieve Weather Data
2) Objective 2: Deliverable 2: Create a Customer Travel Destinations Map
3) Objective 3: Create a Travel Itinerary Map

## Resources

* Data Source: [Weather_Database.ipynb](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Weather_Database/Weather_Database.ipynb), [Vacation_Search.ipynb](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Search/Vacation_Search.ipynb) and [Vacation_Itinerary.ipynb](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Itinerary/Vacation_Itinerary.ipynb)
* Data Files: [WeatherPy_Database.csv](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Weather_Database/WeatherPy_Database.csv), [WeatherPy_vacation.csv](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation.csv) and [cities.csv](https://github.com/DougUOT/World_Weather_Analysis/blob/main/weather_data/cities.csv)
* Output Maps: [WeatherPy_vacation_map.png](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png), [WeatherPy_travel_map.png](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.PNG) and [WeatherPy_travel_map_markers.png](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.PNG)
* Software: Python 3.8.8, Anaconda 4.11.0, Jupyter Notebook 6.4.6, Pandas 1.3.4, Matplotlib 3.4.3, Gmaps 0.9.0, Requests 2.26.0 and Numpy 1.20.3

## Basic Project Plan

Here is a blueprint of the primary project plan:

* Task: Collect and analyze weather data across cities worldwide.
* Purpose: PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
* Method: Create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real-time. This process will entail collecting, analyzing, and visualizing the data.

The data analysis will be parsed into three principal parts or stages:

1.1. Collect the Data

* Use the NumPy module to generate more than 1,500 random latitudes and longitudes.
* Use the citipy module to list the nearest city to the latitudes and longitudes.
* Use the OpenWeatherMap API to request the current weather data from each unique city in the list.
* Parse the JSON data from the API request.
* Collect the following data from the JSON file and add it to a DataFrame:
  * City, country, and date
  * Latitude and longitude
  * Maximum temperature
  * Humidity
  * Cloudiness
  * Wind speed

2.1 Exploratory Analysis with Visualization

* Create scatter plots of the weather data for the following comparisons:
  * Latitude versus temperature
  * Latitude versus humidity
  * Latitude versus cloudiness
  * Latitude versus wind speed

* Determine the correlations for the following weather data:
  * Latitude and temperature
  * Latitude and humidity
  * Latitude and cloudiness
  * Latitude and wind speed

* Create a series of heatmaps using the Google Maps and Places API that showcases the following:
  * Latitude and temperature
  * Latitude and humidity
  * Latitude and cloudiness
  * Latitude and wind speed

3.1 Visualize Travel Data

Create a heatmap with pop-up markers to display information on specific cities based on a customer's travel preferences. Complete these steps:

  * Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
  * Create a heatmap for the new DataFrame.
  * Find a hotel from the cities' coordinates using Google's Maps and Places API, and the Search Nearby feature.
  * Store the name of the first hotel in the DataFrame.
  * Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.

## Results & Code

### 1) Objective 1: Retrieve Weather Data

#### 1.1. Collect the Data

* Use the NumPy module to generate more than 1,500 random latitudes and longitudes.
* Use the citipy module to list the nearest city to the latitudes and longitudes.
* Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
* Parse the JSON data from the API request.
* Collect the following data from the JSON file and add it to a DataFrame:
  * City, country, and date
  * Latitude and longitude
  * Maximum temperature
  * Humidity
  * Cloudiness
  * Wind speed

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_fig1.PNG)

Retrieve Data

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_fig2.PNG)

Data retrieving and skipping city that was not found

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_fig3.PNG)

Creating a Panda DataFrame with weather parameters by city and latitudes

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_fig4.PNG)


### 2) Objective 2: Deliverable 2: Create a Customer Travel Destinations Map

#### 2.1 Exploratory Analysis with Visualization

##### * Create the scatter plots of the weather data for the following comparisons:
  * Latitude versus temperature

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2fig1.PNG)

  * Latitude versus humidity

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2fig2.PNG)

  * Latitude versus cloudiness

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2fig3.PNG)

  * Latitude versus wind speed

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2fig4.PNG)

##### * Determine the correlations for the following weather data:

We use the geographic coordinate system (GCS) to reference any point on Earth by its latitude and longitude coordinates. All latitude lines above the equator are considered as a Northern Hemisphere. All latitude lines below the equator are considered as Southern Hemisphere. We used Linear Regression to Find the Relationship Between Variables or weather parameters.

  * Latitude and temperature

Northern Hemisphere for Max Temp

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr1.PNG)

Southern Hemisphere for Max Temp

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr2.PNG)

  * Latitude and humidity

Northern Hemisphere for Humidity

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr3.PNG)

Southern Hemisphere for Humidity

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr4.PNG)

  * Latitude and cloudiness

Northern Hemisphere for Cloudiness

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr5.PNG)

Southern Hemisphere for Cloudiness

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr6.PNG)

  * Latitude and wind speed

Northern Hemisphere for Wind Speed

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr7.PNG)

Southern Hemisphere for Wind Speed

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Module6_2figcorr8.PNG)


##### * Create a series of heatmaps using the Google Maps and Places API that showcases the following:

  * Latitude and temperature

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Heatmap_Temperature.png)

  * Latitude and humidity

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Heatmap_percent_humidity.png)

  * Latitude and cloudiness

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Heatmap_percent_cloudiness.png)

  * Latitude and wind speed

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Heatmap_wind_speed.png)


### 3) Objective 3: Create a Travel Itinerary Map

#### 3.1 Visualize Travel Data

Create a heatmap with pop-up markers to display information on specific cities based on a customer's travel preferences. Complete these steps:

  * Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
  * Create a heatmap for the new DataFrame.

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Code_Pandas_Dataframe_min_max_temp.PNG)

  * Find a hotel from the cities' coordinates using Google's Maps and Places API, and the Search Nearby feature.

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Code_Dataframe_Findhotel.PNG)

  * Store the name of the first hotel in the DataFrame.

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Code_Store_name_First_hotel_Data_Frame.PNG)

  * Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.

Heatmap of temperatures for the vacations spots 

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/2Heatmap_temperature_vacation_spots.png)

Heatmap of temperatures for the vacations spots with pop-up markers for each city, with hotel name, city, country and Max temp.

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/2Heatmap_temperature_vacation_spots%20and%20markers.png)

#### 3.2 Create a Travel Itinerary Map

Creating a vacation itinerary to travel between four cities. The country selected was Brazil. The cities selected were Rio de Janeiro, Vila Velha, Ilheus and Jardim.

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Obj3_Itinerary_four_citiescode.PNG)

Adding information on the markers on map, such as city name, the country code, the weather description and maximum temperature for the city

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Resources/Images/Obj3_Itinerary_four_citiescode2.PNG)

Follow below the Itinerary map and route between the four cities mentioned above. The route starts in Rio de Janeiro and finishes and the same town. The letter A is related to the start point, and the letter E is the endpoint on the markers. The second waypoint in Vila Velha represents the travel map as the letter B. The third waypoint is Ilheus or letter C. The last waypoint in Jardim is the letter D. After the last way stop, the route continues until Rio de Janeiro, at the same start point as mentioned above.

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.PNG)

Follow below the map, with information on the markers, such as city name, the country code, the weather description and maximum temperature for the city

![](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.PNG)

## Limitations

Related to section 3.2 Create a Travel Itinerary Map, due to the zoom and scale of the map used in this project (file: [WeatherPy_travel_map.PNG](https://github.com/DougUOT/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.PNG)), the letter E overlaps with the letter A.  Applying the zoom on the map will make it possible to confirm that both letters are at the same point; this is because the starting point and the endpoint on the route refer to the same city, Rio de Janeiro.


