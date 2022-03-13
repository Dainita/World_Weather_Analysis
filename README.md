# World_Weather_Analysis
Module 6

## Overview 

### Purpose
After creating a beta test module for searching vacation spots by temperature, we moved on to add the city selection function with travel itninerary and a travel route. These added features will allow the traveler to plan the vacation with minimal input or assistance from a travel agent. Vacationers can plan trips around the world with the click of a few buttons. 

## Analysis and Challenges

### Analysis of Weather Data Retrieval
API call was used to retrieve weather data and current weather description from OpenWeatherMap to create the new dataframe and export it to a WeatherPy_Database.csv. This csv file contains the information needed to create the travel destinations map. 

![WeatherPy_Database.csv](https://github.com/Dainita/World_Weather_Analysis/blob/main/Weather_Database/WeatherPy_Database.csv)

### Analysis of Travel Destinations Map
WeatherPy_Database.csv was read into the file and the loc method was used to retrieve the city data for the corresponding coordinates.  A new dataframe was created to hold the hotel names and a for loop was used to iterate through the data to matche the hotels with the city and coordinate data. An info box template was used to select the desired format of map markers and a marker layer map with a pop-up marker for each city was created.

![WeatherPy_vacation_map](https://github.com/Dainita/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

### Analysis of Travel Itinerary Map
The Directions API was enabled in OpenWeatherMap to retieve the route for the vacation itinerary and the WeatherPy_vacation.csv was imported. Code from the Travel Destinations Map was refactored to create a marker layer map of the vacation search results.
![WeatherPy_travel_map](https://github.com/Dainita/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)
Four cities were selected from this map, Tomatlan, Coahuayana, Acapulco, and Puerto Escondido. A new dataframe was created for each city, then the to_numpy function was used to retrieve the coordinates of these cities as tuples. This data was then used to create a 	directions layer map. The concat function was used to create a combined data base of the four destinations included in the itineray, then, used to create an updated marker layer map with a pop-up marker for the four cities to be visited.

![WeatherPy_travel_map_markers](https://github.com/Dainita/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)

## Results
A vacation itinerary planner for selecting travel locations based on temperature that provides the travel route and nearest hotel data. Travelers can plan a vacation with a few simple selections that will provide important weather and lodging information. 
