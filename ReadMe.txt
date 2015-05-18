Welcome to the DataAnalysisRestaurant-Crime wiki!

This project provides an analysis of relation between two datasets namely 1. “Active Food Establishment Licenses” 2. “Crime Incident Reports”

The analysis will determine how crime is related with respect to restaurants in boston. It will answer questions line "Which is the safest restaurant in Boston?" or "What is the most dangerous Dunkin Donuts in Boston?"

Implementation: We are using the python pandas library for data analysis. Following are the steps performed during analysis.The raw data is in csv format. We will use the "Location" column information to link the two datasets

Loading and Cleaning the data.

Load the data into restaurant and crime data into data frame
Filter out the rows which have null location
Add new column of Zip code to the crime data frame which is computed from the Latitude and Longitude

Finding relationship

Join the restaurant and crime data sets on 'Zip Code'. This will return a data frame with information for crime incidents in the area for each restaurant.
Group the by restaurants and find the count of crimes incidents in the area. This pointer indicates how dangerous the area is.For e.g IncidentCount 10 indicates the restaurant is dangerous with frequent crimes in its area.
Exporting the result The result is exported in JSON file.