---
title: "Vehicle Length (Freight)"
---
The primary purpose of collecting vehicle length data is to analyze freight versus non-freight traffic where vehicle lengths less than 20 ft are non-freight traffic. PORTAL uses "freight" to distinguish these two traffic types.

_Data Availability Note:_ There were periodic outages of the freight data feed in Fall 2017. In particular, there was an extended outage from 2017-09-30 through 2017-10-27.

## Learning objectives
By the end of the tutorial users should be able to:

* select a station and set plotting parameters
* explore and understand what percent of traffic is freight versus non-freight, the change over time of of freight versus non-freight traffic, and vehicle counts by speed ranges over time
* download data used in rendering plots

### Step 1: Select a station
Users can select a station by either choosing a station from the "Station" drop down menu or by clicking on a station on the map represented by the green dots. Vehicle length data is currently only available from ODOT.

### Step 2: Select a start and end date
Select a start and end date of interest by either entering the date under "Start" and "End", or by using the calendar menu.

### Step 3: Select a metric of interest
Select the metric of interest by using the drop down menu under "Measure". The two metric options for plotting are either vehicle length or speed.  

### Step 4: Select a resolution
Select the time resolution of interest by using the drop down menu under "Resolution". The options are 15 minutes, one hour, and one day.

#### _Example_
<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle-length-img1" alt = "">
  <figcaption>Figure 1. Screen shot of the <i>Vehicle Length</i> page showing the following set parameters for the Multnomah (2R304) to NB 1-5 station: start and end week is set to 2018-04-01 and 2018-04-14, respectively, and vehicle length with a resolution of one hour.</figcaption>
</figure>

### Step 5: Select type of plot

Once a type of plot is selected (description on the types below) then click on the "Update" button to render the plot. Once the plot is rendered, users have the option to zoom in by clicking and dragging the cursor the length of the desired time frame.

#### Vehicle length
The "Standard" plot option will show daily vehicle length count based on four distinct binned lengths (0, 20] ft, (20, 30] ft, (35, 60] ft, and (60, 120] ft. The plotted vehicle length ranges can be turned on and off by clicking on the individual legend keys. Individual point values will appear in a pop-up window by moving the cursor to the desired point.

#### _Example_
<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle-length-img2" alt = "">
  <figcaption>Figure 2. Screen shot of the <i>Vehicle Length</i> page showing the "Standard" vehicle length plot at hourly resolution for the Multnomah (2R304) to NB 1-5 station from 2018-04-01 through 2018-04-14; the pop-up window shows the counts for each vehicle length range.</figcaption>
</figure>  

The "Aggregate" plot option will prompt two additional selection criteria, "Measure Ranges", and "Week Days". "Measure Ranges" provides the option of aggregating the selected ranges. "Week Days" provides the option of selecting which days of the week should be aggregated. The start and end date will default to the month and year of the initial start and end date. The resulting plot will show the total vehicle count of the selected aggregated options over a 24-hour period for an entire month. The default selection is all days of the week and all vehicle length ranges.

#### _Example_
<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle-length-img3" alt = "">
  <figcaption>Figure 3. Screen shot of the <i>Vehicle Length</i> page showing the "Aggregated" selection criteria and plot for vehicle length. The plot shows the total vehicle counts for all the Saturdays and Sundays in the month of 2018-04 for all vehicles in the ranges of (20, 35] and (35, 60] ft over a 24 hour period. </figcaption>
</figure>

#### Vehicle speed
The "Standard" option will show the daily vehicle speeds binned by 10 mph increments from (0, 10] to (90, 100] mph. Once plotted, each speed range can be turned on and off by clicking on the desired legend key.

#### _Example_
<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle-length-img4" alt = "">
  <figcaption>Figure 4. Screen shot of the <i>Vehicle Length</i> page showing the "Standard" selection criteria and plot for vehicle speed. The plot shows the total vehicle counts for all speed ranges at 15 minute resolution. To examine data over a finer time scale, a selection is made by clicking and dragging across the plot to highlight 2018-04-05 through 2018-04-08.</figcaption>
</figure>

#### _Example_
<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle-length-img5" alt = "">
  <figcaption>Figure 5. Screen shot of the <i>Vehicle Length</i> page showing the "Standard" selection criteria and plot for vehicle speed after zooming in to the selected time frame of 2018-04-05 through 2018-04-08. The resent button in the upper right corner will zoom out to the original plot.</figcaption>
</figure>  


The "Aggregate" plot option will prompt two additional selection criteria, "Measure Ranges", and "Week Days". "Measure Ranges" provides the option of aggregating the selected ranges. "Week Days" provides the option of selecting which days of the week should be aggregated. The start and end date will default to the month and year of the initial start and end date. The resulting plot will show the total vehicle count of the selected aggregated options over a 24-hour period for an entire month. The default selection is all days of the week and all vehicle speed ranges.

#### _Example_
<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle-length-img6" alt = "">
  <figcaption>Figure 6. Screen shot of the <i>Vehicle Length</i> page showing the "Aggregated" selection criteria and plot of vehicle speeds for 2018-04 with (0, 10] and (80, 100] unselected, and Friday and Saturday selected, over a 24 hour period.</figcaption>
</figure>  

### Step 6: Download data
Click on the "Download" button to download data used to generate each type of plot.

_Vehicle length_
The "Standard" data download will export one file with a date and time stamp and the corresponding vehicle count for each vehicle length range (five columns). The "Aggregate" data download will export the aggregated data used to generate the plot; a column with the 24-hour time stamp and a column of total vehicle counts (two columns).

_Vehicle speed_
The "Standard" data download will export one file with a date and time stamp and the corresponding vehicle count for each vehicle speed range (11 columns). The "Aggregate" data download will export the aggregated data used to generate the plot; a column with the 24-hour time stamp and a column of total vehicle counts (two columns).

## Resources

Last updated: 2018-09-20
