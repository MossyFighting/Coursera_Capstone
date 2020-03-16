# Coursera_Capstone
# Open a restaurant in urban district, Hanoi
### Applied Data Science Capstone by IBM/Coursera
## Problem statement
In order to answer the question, where should a client/an investor invest to open a restaurant in urban district of Hanoi with higher chance of getting more profits and reduce the risk of being losing their money in the long-term. One of the good anwsers to this question is data science and some available software tools/algorithms. By using some analytics, some solutions can give to the clients to have a better understanding about their problems.
## Data presentation
1. Data about each administrative unit of Hanoi is obtained from following link. ([here](https://en.wikipedia.org/wiki/Hanoi))
2. Housing price for each neighborhood in Ha noi can be found at [lease price in Hanoi](https://mogi.vn/gia-nha-dat).
3. The latitute and longitude coordination for each neighborhood can be retrieved from geopy that is a open source library using Python.
## Methodology
1. To start, the first thing to mention is, both **numpy** and **pandas** are used to manipulate the data and dataframe.
2. The next step, the administrative units of Hanoi are obtained by **scraping** the wikipedia webpage. And then, the price of housing in each district is done by scraping another website that mentioned in step 2. of Data presentation. In both cases, **Beutifulshop** from ps4 open source package are used to carried out the task.
3. In order to explore the data more convenient, some figures have been generated using the open source package like **matplotlib.pyplot**.  
4. An important metric like population density is computed and add to the data frame from the total population and area of each district.
5. In order to retreive latitude and longitude from each administrative unit of Hanoi, the **geopy.geocoders.Nominatim** is used and then two columns latitude and longitude are added to the dataframe.
6. When the collected data in data frame are fulfilled, all longitude and latitude for each district are plotted and visualized on the real map using **folium** open source package.
7. In this project, we are interested in the venues like restaurants to see how they distributed across the map of Hanoi, so the **Foursquare API** is very useful to deploy.
8. To extract the meaningful pattern of all restaurants in Hanoi, the **kMeans clusterers** (in the **sklearn.clusters** open source package) is used. To decide which number of clusters we should use, the classical method like **Elbow method** has been used and the graph show the Inertia depending on the number of clusters is presented.
9. A decision has been done based on the available data obtained after process and use aforementioned method.
10. Some notes about pros and cons that have been carried out draw a conclusion for this project
