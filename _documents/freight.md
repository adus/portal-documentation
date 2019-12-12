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

## Additional Resources
- [User manual]({{ site.url }}{{ site.baseurl }}/assets/pdfs/FreightUserManual-11-6-16.pdf)
- Presentations:
  - Monsere, Chris. [Adding Continuous Truck Counts to the Regional Data Archive (PORTAL)]({{ site.url }}{{ site.baseurl }}/assets/pdfs/Monsere_FreightTAC.pdf). 2010 May 12.
  - Monsere, Chris. [Adding Continuous Truck Counts to the Regional Data Archive (PORTAL)]({{ site.url }}{{ site.baseurl }}/assets/pdfs/Monsere_Transport071410.pdf). 2010 July 14.
  - Monsere, Chris. [Permanent Freight Data Collection Infrastructure and Archive System]({{ site.url }}{{ site.baseurl }}/assets/pdfs/Monsere_Transport040813.pdf). 2013 April 10.
- [State of the Practice Review]({{ site.url }}{{ site.baseurl }}/assets/pdfs/Deliverable1_ReviewofStateofPractice.pdf))
- [TCU Manual](({{ site.url }}{{ site.baseurl }}/assets/pdfs/TCU_Documentation_Draft_06052013.pdf)
- Map: [Freight Volumes and Freeway Detectors (March 2012)]({{ site.url }}{{ site.baseurl }}/assets/pdfs/FreightVolumesandFreewayDetectors.pdf)
- MnDOT. [Loop- and Length-Based Vehicle Classification, Federal Highway Administration - Pooled Fund Program TPF-5(192)]({{ site.url }}{{ site.baseurl }}/assets/pdfs/Minge_2012_MNDOT_Length-based_PooledFund.pdf). 2012 November.

The figure below, from the pool-fund study (MnDOT, 2012), provides an illustration of the association between vehicle length and vehicle class. The table below lists the class names and is taken from a MAG study [(2012)](https://www.azmag.gov/Documents/TRANS_2011-02-25_Federal-Highway-Administration-Vehicle-Classes-With-Definitions.pdf), which also provides descriptions of the vehicle classes. The vertical red lines in Figure 7 show one potential set of length bins and how those length bins capture different vehicle classes. For example, the "short" bin in this figure will capture all Class 2 vehicles (passenger cars), most Class 3 vehicles (other two-axle, four-tire single unit vechicles), some Class 5 vehicles (two-axle, six-tire single-unit trucks), and a very few Class 6 vehicles (three-axle single-unit trucks).

Table 1: Class names and descriptions from MAG Internal Truck Travel Survey and Truck Model Development Study.  

| Class | Description |
| --- | --- |
| Class 1 | Motorcycle |
| Class 2 | Passenger cars |
| Class 3 | Other two-axle, four-tire single unit vehicles |
| Class 4 | Buses |
| Class 5 | Two-axle, six-tire, single-unit trucks |
| Class 6 | Three-axle single-unit trucks |
| Class 7 | Four or more axle single-unit trucks |
| Class 8 | Four or fewer axle single-trailer trucks |
| Class 9 | Five-axle single-trailer trucks |
| Class 10 | Six or more axle single-trailer trucks |
| Class 11 | Five or fewer axle multi-trailer trucks |
| Class 12 | Six-axle multi-trailer trucks |
| Class 13 | Seven or more axle multi-trailer trucks |  

<figure class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/vehicle_classes_chart.png" alt = "">
  <figcaption>Figure 7. Potential set of length bins.</figcaption>
</figure>

Last updated: 2019-12-12
