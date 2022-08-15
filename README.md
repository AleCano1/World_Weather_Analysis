# World_Weather_Analysi
PlanMyTrip desired to collect and analyze weather data across cities worldwide with the objective of recommend ideal hotels based on the climatic preferences of the clients. PlanMyTrip  is a company of leading travel technology specializing in Internet-related services in the hotel and lodging industry.

## Overview of Project 
### Purpose 
The purpose of the project is to collect cities worldwide and their weather from OpenWeather API, to plot the relationship between latitudes and the weather, to predict the best time of the year it's better to plan a vacation, to choose the best city to have a vacation based on the weather criteria, map these cities using Jupyter G maps and Google Place API, to add the weather description to the weather collection, to choose four cities and create an itinerary. In this project, analytical, visualization, and statistical skills were used.


### Tools and Tecnhologies: 
During this project was used  Jupyter Notebook, Pandas Library, Matplotlib, Numpy, CitiPy, Python Requests, APIs and JSON Traversals.

### Data description
Based on the collected data from OpenWeather API, there were created a DataFrame with some information about random cities and their weather in real time, it has nine columns plus index:
Index, City, Country, Lat, Lng, Max Temp, Humidity, Cloudiness, Wind Speed and Current Description.

<img width="482" alt="Dataframe" src="https://user-images.githubusercontent.com/96165500/184736233-0467268f-f1f9-4aeb-a7e0-bbcf059f779d.png">

## Results 
To achive the puprose of this project, there were a input to prompt the user to enter minimum and maximum temperature criteria.

    min_temp = float(input("What is the minimum temperature you would like for your trip? "))
    max_temp = float(input("What is the maximum temperature you would like for your trip? "))
    
After the data was filtered based on the criteria, was possible to use google API, to call a hotel Name with a spesific parameters, as 5000 meters of radius, specifiying the latitud and longitude of the cities DAtaFRame created before. For this new information there were created a new DataFrame with name of the Hotel added.
With this information was creted a gmap 


## Summary
