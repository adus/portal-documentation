---
title: "Stations"
---
The _Stations_ section allows users to get travel time, vehicle miles traveled, speed, and volume for a specific station. There are three different pages associated with this section.

## Learning objectives
By the end of the tutorial, users will be able to:

* select a station
* understand, navigate, and use the _Explore_ options on the _Two Quantity Chart_ page

### Step 1: Select a station
Select any single station on the map. The stations are grouped by the direction of traffic (north, south, east, west). Once a station has been selected a pop-up will provide the name of the station and location, and a link to view more information (Figure 1).

<figure align = "center">
<figcaption>Figure 1. Screen shot of <i>Stations</i> page.  </figcaption>
<img src="https://github.com/adus/portal-documentation/blob/master/images/stations-images/stations_page1.png" width="650">
</figure>

### Step 2: Current station information
<figure align = "center">
<figcaption>Figure 2. Screen shot of second <i>Stations</i> page with summary information of a selected station. Outlined boxed areas in color are referenced in text.</figcaption>
<img src="https://github.com/adus/portal-documentation/blob/master/images/stations-images/stations_page2a.png" width="650">
</figure>

Clicking on the _Click here to view more_ link will open to a summary of current station information page. Figure 2 shows a screen shot of the summary stations page. The top panel shows a more detailed map and the location of the station designated by a star. Additional information provided on this page include highway name, number of lanes, milepost of the station location, and the length of the station data it represents. If available, the option to click on the downstream station, the station for the opposite direction, or the upstream station will be highlighted available. If these options are unavailable, the buttons will be grayed out (Figure 2, outlined in red box).

The bottom left panels show the vehicle hours traveled (VHT) and travel time. The bottom right panel shows the speed and volume per lane per hour (VPLPH). Data presented in these two panels shows the current daily information. For historical and additional information click on the _Explore_ buttons located at the upper left corner of either of the plots; this will continue to the final _Stations_ page to visualize two different quantities and download data.

### Step 3: Two quantity chart
The _Two Quantity Chart_ page provides more detailed information about the station, options for plotting two different quantities, concomitant weather data, and the option to download data.

__Data and visualization parameters__  
<figure align = "center">
<figcaption>Figure 3. Screen shot the <i>Stations: Two Quantity Chart</i> page showing all parameter options on top, two quantity chart in the middle, and weather data below.</figcaption>
<img src="https://github.com/adus/portal-documentation/blob/master/images/stations-images/stations_page3a.png" width="500">
</figure>

_Date Range_
In addition to the _Start_ and _End_ date options, days of the week can also be selected by clicking on each button. The default selection is all days of the week and today's date for the _Start_ and _End_ date.

_Time Range_
To select a specific time range of interest use the _Start_ and _End_ inputs (e.g. peak PM traffic or peak AM traffic). The default selection is set to all day.

_Quantities_
The default quantities plotted are speed and VPLPH; other quantities are average volume, occupancy, vehicle miles traveled (VMT), VHT, travel time, and delay.

_Configuration_
Select the temporal resolution of interest (20 sec, 5 min, 15 min, 1 hour, 1 day, 1 month, 1 year). Data are originally recorded at 20 second intervals. If the _Group_ parameter is set to _Yes_ then data are aggregated based on day of week selection under _Date Range_. If the _Group_ parameter is set to _No_ then data are visualized as continuous along the x-axis according to the date and time selected.

_Lanes_
In the direction of travel, the lane number starts from the left and goes to the right (e.g. the far left lane is lane 1). The options for plotting data is either by one lane at a time or aggregated across all existing lanes. The option for plotting data by lanes is currently unavailable. However, indiviudal lane data can be downloaded by clicking on the _Download All Data_ button at the bottom of the plot.

_Example_
<figure align = "center">
<figcaption>Figure 4. Screen shot of the set parameter options for the two quantity chart where <i>Group</i> is set to <i>Yes</i>.</figcaption>
<img src="https://github.com/adus/portal-documentation/blob/master/images/stations-images/stations_page3b.png" width="650">
</figure>

_Example_
<figure align = "center">
<figcaption>Figure 5. Screen shot of the set parameter options for the two quantity chart where <i>Group</i> is set to <i>No</i>.</figcaption>
<img src="https://github.com/adus/portal-documentation/blob/master/images/stations-images/stations_page3c.png" width="650">
</figure>

### Step 4: Download data
There are five types of data available to download:
Each row of data for the _Download Data_ and _Download All Data_ options is determined by the temporal resolution selected.

_Download Data_ is the data that is shown on the selected plot. (e.g. If plotted data are aggregated hourly for speed and VPLPH, then the data downloaded by this option is the aggregated data for those two quantities).

_Download All Data_ is the unaggregated data used to generate the selected plot. Individual lane data can be found in this dataset.

_Download Stations Metadata_ is metadata for all stations available in PORTAL. Attributes for stations metatdata are station_id, agencyid, highwayid, highwayname, milepost, description, upstreamstation, downstreamstation, oppositestation, longitude, and latitude. More information about stations metadata can be found [here](https://github.com/adus/portal-documentation/blob/master/documentation/downloads.md#stations-metadata).

_Download Detectors Metadata_ is metadata for all detectors available in PORTAL. Attributes for detectors metadata are detectorid, stationid, stationname, lanenumber, highwayid, highwayname, and milepost. More information about detectors metadata attributes can be found [here](https://github.com/adus/portal-documentation/blob/master/documentation/downloads.md#detector-metadata).

_Download Weather Data_
Weather data attributes include temperature (F), windspeed (mph), visibilitymiles, precipitation (1/10 inch), name (null), and displayvalue (null).


[Feedback](https://github.com/adus/portal-documentation/issues)  
[Back to Table of Contents](https://github.com/adus/portal-documentation)  
Last updated: 2018-07-27
