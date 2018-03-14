## March 14th: Spatial Data

### Introduction

Today we're going to be getting into the nitty gritty of turning regular old data into **spatial data** that's ready to be analyzed, mapped, or visualized. This is tedious, but it is also an absolutely crucial step that often can take up most of your time. Getting experience with this process will hopefully save you some time down the road. The big theme of today is exploring the pitfalls, trade-offs, and challenges that come with trying to package informat into a "usable" format for a computer. 

In other words:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Updated Turing Test concept:<br>A spreadsheet of dates, hand-entered by interns more than a decade ago, featuring such well-known time formats as &quot;1996ish&quot;, &quot;1941/xd01944&quot;, &quot;1955?&quot; and &quot;WWII.&quot;<br>I&#39;m not worried about AI until someone shows me the algorithm that can make sense of this. <a href="https://t.co/IhzofigX2b">pic.twitter.com/IhzofigX2b</a></p>&mdash; Brooke Watson (@brookLYNevery1) <a href="https://twitter.com/brookLYNevery1/status/954368989181902848?ref_src=twsrc%5Etfw">January 19, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


### Getting The Data

We'll be using data from Caroline's project that she has generously agreed to share. We're going to be looking at this data in the most common form that data currently takes: the ubiquitous spreadsheet. Although many researchers have moved away from spreadsheet software like Microsoft Excel (and with good reason), it's still far and away the most common format that you'll find spatial data. It also offers a fairly accessible way to record and edit data. For today, we'll be using Google Sheets. Upload the file, make a duplicate version, and rename the new version without any spaces in the file name.  

### Reconnaissance and Planning

At this stage, you want to explore the dataset and get a feel for what's in it and how it's structured. This is obviously much more important if you have not collected the data yourself. Tip: Like any software, it's easier to navigate around a spreadsheet with keyboard shortcuts: [Google Keyboard Shortcuts](https://support.google.com/docs/answer/181110?co=GENIE.Platform%3DDesktop&hl=en)

- What does each row represent?
- What does each column represent? 
- Where is the spatial information in this data?
- Are there potential hurdles/challenges to this dataset - either for you (the scholar) or a computer? 
- Finally, plan out your next steps. What are the different tasks you will need to complete to get this spreadsheet into something that you can put onto a map? 

### Cleaning the Data

Although the data is quite legible to a human reader, we need to try and "clean" it and modify it so that it is easily digestible from the perspective of a computer. This is often one of the most laborious and time-intensive phases of a project. 

Simplify:

- Get rid of visual formatting (ex. merged cells, etc.)
- Make sure the first row is column headers
- Get rid of extra whitespace using the `TRIM()` function
- Replace empty cells in the two date columns with `N/A` values using the `IF()` function

Standardize:

- Use `Find and Replace` to begin putting all the addresses into the same format (ex. "Street" vs. "St.", etc.) 
- Use `CONCATENATE()` function to add in data to groups of addresses (ex. adding state abbreviations to multiple addresses in a row)

### Mappable Data

Now we need to make this spreadsheet into a *spatial dataset.* Given that each of the records are individual locations with addresses, we need to assign Latitude/Longitude coordinates to it: it's "actual" pinpoint location on a globe. This is a process known as *geocoding* - looking up addresses or places in existing databases to try and generate specific coordinates. There are a lot of different services out there for geocoding data, and most of them cost money or impose quotas on how many addresses you can geocode at a time. For now, we're going to use a [lightweight option](https://www.doogal.co.uk/BatchGeocoding.php) that allows us to simply copy and paste our data into an online form. Note: in the "Separate text output with" option, select Tabs. 

Although you can see the results of the geocoding process on a map, what we want is the underlying datafile. Either copy and paste the resulting data into your spreadsheet or download the Text file. We now have two new columns: `Latitude` and `Longitude` that hold the key to being able to pin these places onto a map. 

### Your Own Data

For the remainder of class, pair off and delve into your own datasets for your final projects. Either walk through your existing data or your plans for how you're going to collect it. For each person, try and hammer out a concrete plan for moving from the initial data to a final version of spatial data that is "usable" for a computer. I will be circulating to answer questions or provide feedback. 
