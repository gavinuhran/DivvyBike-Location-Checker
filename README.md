# DivvyBike Location Checker
## Created by Gavin Uhran
### Description
DivvyBike Location Checker is a program that assists users in finding nearby DivvyBike stations, which are located throughout the downtown Chicago. DivvyBike stations contain rent-able bikes, that can be used to quickly navigate the city in an environmentally-friendly fashion. This program determines a user's location, and provides directions to the five nearest DivvyBike stations.

### How it Works
The program first prompts the user to input their location as a text field using the **Interact** python library. An example of a great input would be an actual address or a landmark, such as "The Buckingham Fountain" or "Sheraton Hotel Chicago". The **geopy.geocoders** python library then matches the user's input to a pair of latitude and longitude coordinates. 

Next, the program imports both the data for the DivvyBike stations in Chicago (https://gbfs.divvybikes.com/gbfs/en/station_information.json) using the **requests** python library and the data for the Chicago's weather conditions by web-scraping a Google search of Chicago's weather. 

A dictionary is created matching each DivvyBike's station name to its distance from the user's location. The distance for each station is found using the **Haversine formula**, which calculates the distance between two pairs of GPS coordinates. The dictionary is then sorted in ascending order. The five nearest stations are displayed to the user, accompanied with the distance to each of the five stations.

When displayed, each of the five stations will have its own implemented Google Maps feature, that provides interactive directions from the user's location to the station. The map is displayed by implementing Google Maps' accessible HTML using the **IPython.display** python library.

### Future Improvements
Moving forward, I would like to improve the program by creating a user interface using the **tkinter** python library.