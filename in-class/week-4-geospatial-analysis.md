## January 31st: Geospatial Analysis

### Introduction

This week we're going to be using Carto like we did in [Week 2]({{site.baseurl}}/in-class/week-2-map-design). We're going to learn some standard types of geospatial analysis. Although the details of the techniques are specific to the Carto software, they are also standard types of analysis that you can do in QGIS or ArcGIS. Once again, the idea is not to give you an expertise over every single kind of geospatial analysis, but to give you hands-on experience with using specific ones. The format for today is going to involve following a few tutorials that Carto provides to its users, but following those same steps using our own data.

For today's class we're going to use two Boston municipal datasets, one of which you used in [Week 2]({{site.baseurl}}/in-class/week-2-map-design). Connect to each of these datasets in your Carto account.

1. [Boston neighborhoods](http://bostonopendata-boston.opendata.arcgis.com/datasets/3525b0ee6e6b427f9aab5d0a1d0a1a28_0) 
- You can import this directly using the GeoJSON option under API.
2. [Code Enforcement Violations from 2017]({{site.baseurl}}/in-class/downloads/cepviolations_2017.csv) 
- Note: you should already have this connected as a dataset in Carto from Week 2. Otherwise, you can connect it again by downloading it and uploading it as a new dataset.

### Exercise I. Intersecting Layers

The first tutorial is the [Intersect Second Layer](https://carto.com/learn/guides/analysis/intersect-second-layer/) tutorial on Carto. 

We're going to try and go through it using our own data. The idea is that we want to run a spatial analysis that will count the number of Code Enforcement Violations from 2017 (represented by the ~52,000 points in our `cepviolations_2017.csv` file) in different Boston neighborhoods (the Boston neighborhoods polygon layer). This is going to add a column to our Boston neighborhoods layer that counts up all of the points that fall within its boundaries. Try to come up with the following:

1. Which two neighborhoods had the most CEP violations in 2017? (Hint: look at the Data view of your neighborhoods layer to see the new column of counts that was added during your Analysis stage)
2. Export the new Boston Neighborhoods layer from your map as a SHP file. You could theoretically then use this new file, with the results of its spatial analysis, in QGIS, ArcGIS, etc. 

### Exercise II. Clusters of Points

For this exercise, we're going to learn how to group points together using k-means clustering. Using the Code Enforcement violations dataset, we'll try to group the ~52,000 code violations into six geographical zones. Follow the Clusters of Points Carto tutorial, but substitute your CEP violations dataset instead of store locations: [https://carto.com/learn/guides/analysis/calculate-clusters-of-points/](https://carto.com/learn/guides/analysis/calculate-clusters-of-points/).

### Exercise III. Finding Centroids

Finally, we're going to combine clustering (Exercise II) with a second step of analysis: finding the centroids of our six new "zones" (clusters) of CEP violations. If we were going to assign six city employees to go around issuing violation tickets in these six areas, where should they be stationed? Basically, what is the most central location in each of these areas ("as the crow flies")? Follow this Carto tutorial, but once again substituting your Boston CEP violations from 2017 rather than New York Citi Bike data: [https://carto.com/learn/guides/analysis/find-centroid-of-geometries/](https://carto.com/learn/guides/analysis/find-centroid-of-geometries/)

Note: You won't be using the "weighting" feature of this analysis, since the violations don't have this kind of quantitative data attached to each individual point. Ignore the steps of `WEIGHTED BY` and `AGGREGATE`.

Create a final map that includes the following elements:

1. All CEP violations from 2017, color coded into six different clusters and resized to small, semi-transparent dots.  
2. The central location of each of these clusters, sized according to how many violations were in that cluster.  
3. A polygon layer of Boston Neighborhoods. Re-run the analysis from Exercise I by counting the number of CEP violations within each neighborhood, and color the different neighborhoods according to the calculated value (changing the transparency to make the your other two layers visible. 
