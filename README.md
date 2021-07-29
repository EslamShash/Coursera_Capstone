# Coursera_Capstone
# The Battle of Neighborhoods

## Introduction
Cairo is a sprawling city, and like you probably noticed in other big cities, not all neighborhoods were created equal.
The aim of this project is to use Foursquare location data to explore and compare neighborhoods of Cairo and use these data to solve a problem.

## Problem Description
If a company is trying to start their own business in Cairo, where would you recommend that they setup their office? It would depend on a lot of factors like what is the type of business? and what are the target customers? 
To help answering these questions we need to know what the most common venues in every neighborhood in Cairo are and what are the similarities and differences between these neighborhoods. 
In this project we will cluster neighborhoods based on the most common venues like Hotels, Historic sites, restaurants, or parks. Which will help any company decide where to locate their office based on the pattern of location of these venues. 

## Target Audiences
Companies or individuals who are trying to find the best neighborhood in Cairo to locate their office based on the most common venues in each neighborhood.

## Data description
I collected the all the neighborhoods in Cairo and their location data from Wikipedia in a CSV file. Then plugged these locations in Foursquare API to get all the venues in every neighborhood within 5 km.
Foursquare API gives a lot of information about every venue, but I only used the Category description of the venue. 


## Methodology
Cairo’s neighborhoods and their latitudes and longitudes was collected from Wikipedia and cleaned and saved into a CSV file. 
Then used Foursquare API to explore areas around center of each neighborhood and find 10 most common venues in each neighborhood. I've set the radius of search to 5000 meters around the center of each neighborhood. 

The result was 3639 venues returned by Foursquare in Cairo. Next step was to create a table, which shows a list of top 10 venues for each neighborhood

The next step is to cluster the neighborhood, so I used K-means clustering algorithm to group neighborhoods, based on the frequencies of venues in each neighborhood. These groups will be used to find similar neighborhoods in Cairo.

From K-Means elbow method we can conclude that an optimal number of clusters would be 4.
I ran the KMeans algorithm on the data and used Folium library to visualize the clustered neighborhoods on Cairo map.

## Results
We managed to cluster the neighborhoods into 5 clusters with each cluster group similar neighborhoods sharing the similar venues categories.

## Discussion
The Foursquare API have a limited venues queries in the free version. If we used the premium version we can increase the radius of search in every neighborhood which will increase the number of venues queried from the API and increase the accuracy of the model in clustering the neighborhoods correctly. 

## Conclusion
Cairo boasts the largest city population in all of Africa and the Middle East, and navigating its vast districts can be a daunting prospect for any one. I’ve picked clustered the most similar neighborhoods, from ancient quarters to affluent modern districts, to help you make the most of any business decision of choosing a place to start your business or just planning a visit to one of these neighborhoods.
While the model didn’t reach high level of accuracy in clustering these neighborhoods, its still a good start in the right direction. 

