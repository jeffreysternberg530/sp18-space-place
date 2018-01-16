### January 17th: Map Design

## Part I. Introduction to the Data

We're going to be learning how to design maps using Carto, a fairly lightweight and flexible web mapping service. To do so, we'll be using municipal data released by the City of Boston to play around with different ways of changing the appearance of that data. The purpose of this exercise is less analytical, and more getting familiar with things like symbology, color, etc. and how to manipulate those features using text-based programming rather than a purely visual interface.

Carto divides its interface into Datasets and Maps. To build a map, you first need to connect to a dataset. Although you can upload your own data, it also allows you to connect to existing ones online. I've chosen three datasets that give you some experience with different *kinds* of map data types (namely: polygons and points), all of them collected and made available by the City of Boston.

*Polygons:*

- Historic Landmarks: Polygon data collected by the Boston Landmarks Commission and released  through the city's Open Data portal. [http://bostonopendata-boston.opendata.arcgis.com/datasets/7a7aca614ad740e99b060e0ee787a228_3](http://bostonopendata-boston.opendata.arcgis.com/datasets/7a7aca614ad740e99b060e0ee787a228_3)

*Points:*

- Code Enforcement Violations: [https://data.boston.gov/dataset/code-enforcement-building-and-property-violations/resource/90ed3816-5e70-443c-803d-9a71f44470be](https://data.boston.gov/dataset/code-enforcement-building-and-property-violations/resource/90ed3816-5e70-443c-803d-9a71f44470be)

You have two options for getting this data into Carto. You can download these datasets under a variety of different formats (KML, spreadsheet, shapefile) and then upload them to Carto. Or you can Connect to the datasets directly within Carto by using their API options (specifically, the GeoJSON link). 

*Note*: the Code Enforcement Violations is a large file encompassing several hundred thousand data points. I've filtered this down to just violations that were recorded in 2017. **You can connect to this dataset directly through Carto: [https://cblevins.carto.com/dataset/cepviolations_2017](https://cblevins.carto.com/dataset/cepviolations_2017)**

## Part II. Changing the Layout (Basic)

Create a new map in Carto and add the three datasets as layers. Play around with the options in the different layers to change their appearance. Some things to try:

- Select a Basemap option that it has less text labelling.

- Change Historic Landmarks to a brown color and make it semi-transparent.

- Change the color of Code Enforcement points to blue.

- Add a Pop-up to the Code Enforcement layer so that you can see a description of the violation when you click on one of the points.

## Part III. Changing the Layout (Advanced) 

Now we'll start changing the layout of the map using CartoCSS, Carto's underlying language for changing the layout and appearance of maps. For those of you familiar with CSS, it is a related language that follows some of the same syntax, but it is not identical. CartoCSS allows you to change the map using a stylesheet syntax. It's easiest to understand by modifying existing code. 

To start, select the Code Enforcement layer and switch from "Values" to "CartoCSS". Then copy and paste the following code blocks:

~~~
#layer {
  marker-width: 4;
  marker-fill: #dc00f4;
  marker-fill-opacity: 0.5;
  marker-allow-overlap: true;
  marker-line-width: 0.5;
  marker-line-color: #FFFFFF;
  marker-line-opacity: 0.5;
  [description='Improper storage trash: res']{
    marker-fill:#0008ff;
  }
  [stno='62'][street='Phillips']{
  	marker-width: 10;
  	marker-fill: #29b100;
  	marker-fill-opacity: 1;
  	marker-allow-overlap: true;
  	marker-line-width: 0.5;
  	marker-line-color: #000000;
  	marker-line-opacity: 1;
  }
  [zoom>14]{
    marker-width: 6;
  }
}
~~~

Try to figure out what these blocks of code are doing - play with different values to see what changes on the map. Once you have a handle on what each of them are doing, try to add your own changes:

- Add code that will allow the user to see all violations for unsafe structures: make these violations larger, give them a brighter color, and make them fully opaque (no transparency). 

- When the user zooms out, it can get hard to differentiate between all the different points. Decrease the size of the points from zoom level 13 onwards so that they are smaller.

- Finally, switch over to the Historic Neighborhoods layer and try to change its appearance using CartoCSS. Highlight all the landmarks in a particular neighborhood (ex. Dorchester, Jamaica Plain, etc.).





