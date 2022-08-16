# World_Weather_Analysis
PlanMyTrip desire to collect and analyze weather data across cities worldwide with the objective of recommending ideal hotels based on the climatic preferences of the clients. PlanMyTrip is a company of leading travel technology specializing in Internet-related services in the hotel and lodging industry.

## Overview of Project 
### Purpose 
The purpose of the project is to collect cities worldwide and their weather, from OpenWeather API, plot the relationship between latitudes and the weather, predict the best time of the year that it's better to plan a vacation, to choose the best city to have a vacation based on the weather criteria, map these cities using Jupyter G maps and Google Place API, to add the weather description to the weather collection, to choose four cities and create an itinerary. In this project, analytical, visualization, and statistical skills were used.


### Tools and Tecnhologies: 
During this project was used  Jupyter Notebook, Pandas Library, Matplotlib, Numpy, CitiPy, Python Requests, APIs and JSON Traversals.

### Data description
Based on the collected data from OpenWeather API, there was created a DataFrame with some information about random cities and their weather in real-time, it has nine columns plus an index:
Index, City, Country, Lat, Lng, Max Temp, Humidity, Cloudiness, Wind Speed, and Current Description.

<img width="482" alt="Dataframe" src="https://user-images.githubusercontent.com/96165500/184736233-0467268f-f1f9-4aeb-a7e0-bbcf059f779d.png">

## Results 
To achieve the purpose of this project, there was an input to prompt the user to enter a minimum and maximum temperature criteria.

    min_temp = float(input("What is the minimum temperature you would like for your trip? "))
    max_temp = float(input("What is the maximum temperature you would like for your trip? "))
    
After the data was filtered based on the criteria, was possible to use google API, to call the Hotel Names with specific parameters, such as 5000 meters of radius, specifying the latitude and longitude of the city, based on the DataFrame created before. For this new information, there was created a new DataFrame, added a column named Hotel Name.
With this information was created a Gmap with the marker layer map with a pop-up marker for each city, holding this information: Hotel Name, City Name, Country, Current Description, and Max temp °F.  

<img width="662" alt="WeatherPy_vacation_map" src="https://user-images.githubusercontent.com/96165500/184743119-70613fc5-3671-421a-8552-3c5d7b3a2e08.png">

The next step, was to create a travel itinerary using the Google Directions API, there were chosen four cities that a customer might want to visit, the cities were Acapulco, Lazaro Cardenas, Tarimoro, and Puerto Escondido, from Mexico. For the route was chosen a start and an ending, also the three stops, to complete the itinerary. To get the latitudes and longitudes was necessary to use the to_numpy() function and list indexing to write code to retrieve the latitude-longitude pairs as tuples from each city DataFrame.
Then, was added a code to create a directions layer map using the variables before, where the starting and ending city are the same city, the waypoints are the three other cities, and the travel_mode is "DRIVING".

        fig = gmaps.figure()
            vacation_itinerary = gmaps.directions_layer(
            start, end, waypoints=[stop1, stop2,stop3 ],
            travel_mode= "DRIVING",
            stroke_color="green", stroke_weight=2.0)

        fig.add_layer(vacation_itinerary)
        fig

The following image shows the map, the route, and the layer marker for each city, defined by Gmaps:

<img width="571" alt="WeatherPy_travel_map" src="https://user-images.githubusercontent.com/96165500/184755421-0fbfdfcf-9c89-47b9-91de-1949ca713470.png">


Finally, there was added a description in the pop-up marker for each city.

<img width="607" alt="WeatherPy_travel_map_markers" src="https://user-images.githubusercontent.com/96165500/184755483-11e1843b-c160-4354-a6cf-881cee1a8fc5.png">

## Summary

This code is helpful for companies who work in the hotel and lodging industry, predicting the weather to offer specific options for the customers can give them an advantage over their competitors. In the same way, the plan of the route for different cities that the clients would like to visit shown on a map is a plus that will be helpful to detail better the vacations.
 Using OpeanWeather and Google APIs is an open option for the analyst to collect and analyze information about the weather and maps. 
For this project in the future, for better performance is possible to add other filters to determine what is what clients are looking for in an advanced search. In this case, the project would be the template to improve the experience of companies in the sector.

### Links

* For more information about OpenWeather APIs visit: https://openweathermap.org/api
* For more information about Google APIs visit: https://console.cloud.google.com/apis/
