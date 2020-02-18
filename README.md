[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/mapbox_logo.PNG)](https://mapbox.com) 
## Intro to Mapbox workshop - Rowan University - Cartography (2/19/2020)

Christopher Pollard, pollardc@rowan.edu, [@CRVanPollard ](https://twitter.com/CRVanPollard)

### Today's goal - make this map
[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/todaysmap.png)](https://api.mapbox.com/styles/v1/crvanpollard/ck6s980mv09oh1iqppo5rusgo.html?fresh=true&title=view&access_token=pk.eyJ1IjoiY3J2YW5wb2xsYXJkIiwiYSI6Ii00ZklVS28ifQ.Ht4KwAM3ZUjo1dT2Erskgg)

### How are we going to get there...
- Overview of Mapbox Studio
- Getting started 
- Importing data into Mapbox Studio
- Visualizing data in Mapbox Studio
- Publishing your style

## Overview of Mapbox Studio
#### Mapbox Studio - https://www.mapbox.com/mapbox-studio/
Design interactive maps that run on any device with Mapbox Studio
- Full basemap design control
- Data visualization
- Publish across platforms

[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/mapboxstudio.png)](https://cartodb.com/editor/)

#### What are people doing with it
[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/strava.png)]
[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/election.png)]
[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/impossible.png)]
[![alt text](https://raw.githubusercontent.com/crvanpollard/Mapbox_Workshop/master/img/alltrail.png)]

## Getting Started

### Set up an account
If you don't have an account, go sign up: [https://cartodb.com/signup](https://cartodb.com/signup)  

### CartoDB Dashboard
This is where you can view and manage your maps and datasets
[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/dashboard.png)](https://cpollard.cartodb.com/me)

## Importing data into CartoDB
### Supported geospatial data formats
http://docs.cartodb.com/cartodb-platform/import-api/importing-geospatial-data/#supported-geospatial-data-formats
- Shapefile
- KML/KMZ
- GeoJson
- CSV
- Spreadsheets (Excel or OpenDocument)
- GPX
- OSM

### Connecting data to CartoDB
There are different ways to import data into CartoDB. It can be files you have stored locally or datasets that you can connect to through Dropbox, Google Drive, Box, Twitter, ArcGIS Server, MailChimp, and SalesForce.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/connect.png)

### Datasets
Today, we are going to use several local datasets that focus on Bicycle Planning.
I have already downloaded and have them ready for our use today. Please copy the following URLs listed below and paste them, one at a time, into your CartoDB importer.

- DVRPC Bicycle Counts ([DVRPC GIS Portal](http://dvrpc.dvrpcgis.opendata.arcgis.com/datasets/f8cf3245754c4b79a89a04a5d278a450_0))
`https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/data/dvrpc_bicycle_counts.csv`

- Philadelphia Bike Network ([Open Data Philly](https://www.opendataphilly.org/dataset/bike-network))
`https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/data/phl_bike_network.zip`

- Census Tract Boundaries 2010 ([Census Geography](https://www.census.gov/geo/maps-data/data/tiger-line.html))
`https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/data/censustracts2010.zip`

- Census 2009 - 2013 ACS Demographic Profiles ([DVRPC GIS Portal](http://dvrpc.dvrpcgis.opendata.arcgis.com/datasets/beb54980293b4c0fa5312f0eb8ffbb1f_0))
`https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/data/asc2013_tract_data.csv`

### Data View
This is where you can view, sort, modfiy, add, and merge datasets together. Very similar to excel and other spreadsheet interfaces. 
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/dataview.png)

### Georeferencing
If you don't have a Geometry field or Lat/Long in your dataset you can use CartoDB's Georeferencing tool to be able to map your data by street address, city name, postal code, administration region, or IP address.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/datageo.png)

### Data Merge
You can also merge datasets that have a common field or attribute that are the same data type <i>(number to number, string to string)</i>.
We will do this with our Census Tract shapefile and ACS 2009-2013 Demographic Profile data.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/datamerge.png)

## Visualizing data in CartoDB
### Style Wizard
CartoDB comes with some great map design tools that allow the user to pick from multple layer styles (simple, cluster, choropleth, category, bubble, torque, heatmap, intensity, and density).
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/mapview_style.png)

### Infowindows
You can also turn on infowindows which allow users to click or hover over a feature and view specific attribute information. You, as the map maker, can select which attributes you allow your users to view.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/mapview_info.png)

### Filters
There is also a function that will allow you to set custom filters or parameters on your layer based off attribute information. For instance, in the map below, the filter is set to only show bicycle counts that have an `ADB` over 100.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/mapview_filter.png)

### CartoCSS
If you wish to have more advanced map styling you can do that with CartoCSS editor.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/mapview_cartocss.png)

### Creating a map of your data
Once you are ready to make a map you click the `Visualize` button and you will now have several map layout tools available. Here you can add a title, text, annotaion, and images, as well as, select from other map options.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/mapview_map.png)

## Publishing your visualization
### Time to share you map with the world
Once you are ready to share your visualization you click the `Publish` button. There are a few options to choose from such as: a link that you can send via email or social media, embed your map into a blog or website, or add it to an existing or custom web mapping applications using CartoDB.js.
![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/publish.png)

## CartoDB Deep Insights (coming summer 2016)
Predictive analytics and on-the-fly visualiztion that will drastically improve CartoDB workflows and analysis.

Key take aways: 
- An actionable dashboard with <b><u>widgets</u></b> (charts and forms)
- <b><u>High Performance Analytics (HPA)</u></b> that not only maps your data but now performs analysis on <b>LARGE</b> amounts of data...really FAST and quick
- Data Augmentation (DA) builds a relationship between 2 datasets and everything that surrounds that data.
Data Augmentation is a series of algorithms that geocode the datasets, performs a spatial join, and adds valuable demographic data (population, income, employment, etc..) to your targeted dataset.

[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/di1.png)](https://cartodb.com/deep-insights/)
[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/di2.png)](https://cartodb.com/deep-insights/)

## CartoDB Resources
#### CartoCSS Reference Sheet - http://ebrelsford.github.io/talks/2014/Methods3/week7/materials/cartocss-reference.pdf
This handy CartoCSS Reference Sheet is a quick guide for beginners to CartoCSS

#### CartoDB Academy - http://academy.cartodb.com
The CartoDB Academy is great for recapping the basics, starting to use their APIs, and growing your design capabilities.
[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/mapacademy.png)](http://academy.cartodb.com)

#### Odyssey - http://cartodb.github.io/odyssey.js/
A simple way for journalists, designers, bloggers, and others to publish stories that combine narratives with map interactions. Allows creative minded people to weave interactive stories with images, maps, and compeling narritives.
[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/odyssey.png)](http://cartodb.github.io/odyssey.js/)

#### Preparing CSV files for use in CartoDB - https://vimeo.com/channels/cartodb/100105203
[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/csv.png)](https://vimeo.com/channels/cartodb/100105203)

#### Using Column Join to Merge Tables - https://vimeo.com/channels/cartodb/100105201
[![alt text](https://raw.githubusercontent.com/crvanpollard/PWT2016_CartoDB/master/img/merge.png)](https://vimeo.com/channels/cartodb/100105201)


