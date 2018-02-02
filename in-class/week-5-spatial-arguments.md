## February 7th: Spatial Arguments

### Introduction

Over the preceding weeks you've gotten experience with creating maps and visualizations and performing some basic geospatial analysis. Today we're going to put all of this together to try and practice how to build spatial arguments. The structure of the exercise will be as follows:

1. Familiarizing yourself with the data
2. Brainstorming possible questions and interpretations
3. Exploring and analyzing the data
4. Presenting a visual argument/interpretation

The goal of this class is **not** to construct an ironclad, unassailable argument. The goal is to walk through the entire process from data to argument, with particular emphasis on the final stage of using visualizations or maps to clearly present a clear argument (even if that argument is entirely wrong). 

### The Data (5-10 minutes)

We're going to once again be returning to municipal datasets from Boston:

1. [Climate Ready Boston's Social Vulnerability dataset](http://bostonopendata-boston.opendata.arcgis.com/datasets/34f2c48b670d4b43a617b1540f20efe3_0). 
2. [Boston Crime Incident Reports from 2016]({{site.baseurl}}/in-class/downloads/crime_2016.csv) 
- Note: This is a subset of a larger dataset that I filtered down to 2016 so that the size is a little bit more manageable. I downloaded [the full data from here](https://data.boston.gov/dataset/crime-incident-reports-august-2015-to-date-source-new-system/resource/12cb3883-56f5-47de-afa5-3b1cf61b257b) - use this link to look at the metadata. 

Take some time to read through the metadata (Details) and the data itself (Table). 

1. What kind of information does this dataset contain?
2. Who created it?
3. When is this data from?
4. What are its sources?
5. Connect the datasets to your Carto account (using the GeoJSON API for #1 and uploading the CSV file for #2)

### Brainstorm (5 minutes)

As a group:

1. Just looking at the type of data (without doing any kind of analysis), brainstorm a list of **three potential interpretations** that might eventually come out of this kind of data. Again, this should not be what you've learned from the data, but simply explicit conclusions one *might* be able to draw using it - use your imagination.
2. Come up with at least **two concrete questions** you could try and answer using these datasets. This can be questions that come from an individual dataset or both of them.

### Exploration and Analysis (10-15 minutes)

Divide the questions up amongst your group members and take a stab at answering them using Carto. As you do so, jot down notes on the following:

1. What observations are you noticing?
2. What challenges are you running into in terms of your ability to answer the question?
3. Is your analysis prompting you to think of any additional questions?

After 10 minutes, reconvene with the full group and share what you've found. **Decide what spatial argument you want to present.** Again: this argument does not have to be perfect, or even strongly backed by evidence. The purpose of today is to practice the *presentation* of arguments in a spatial and visual form.

### Argument (20 minutes)

As a group, construct a map or visualization from the dataset that offers an explicit, rhetorical argument that, as much as possible, can stand on its own. Think hard about what kind of design choices you want to use to convey your message (color, line weight, transparency, etc.)

During the last twenty minutes of class, each group will verbally present their argument to the rest of the class using the map/visualization.