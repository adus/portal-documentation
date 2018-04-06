## Travel Time
Users are able to select a route to compare four weeks of travel time data against average travel time.

### Route Selection
* _Routes_ Users can either use the drop down menu select among several predefined routes, or use the map to create a route by selecting several continuous stations. After clicking on a starting station a blue dot will appear indicating the next available station along a potential route.

* _Start Week_ Only four weeks of data can be plotted and downloaded at one time which includes the selected start week plus the previous three weeks.

Figure 1 shows a selected route along US-26 WB starting at Frog Lake and ending at Arlie Mitchell Road.

<figure align = "center">
<img src="https://github.com/adus/portal-documentation/blob/master/images/transit-time-images/travel-time-img1.png" width="500">
<figcaption>Figure 1. Screen shot of <i>Travel Time</i> page for a route selected along US-26 WB.</figcaption>
</figure>

### Travel Time Options
_Reliability weeks_
The number of reliability weeks chosen determines the number of weeks used to calculate average travel time. Reliability is in reference to the level of consistency of observed average travel time measured daily or for different times of the day. The greater number of reliability weeks selected, the more accurate the travel time. Figure 1 shows the reliability weeks set to six.

_Travel Time_
Travel time reliability is a function of calculating the travel time of cars over five-minute interval periods between two stations, summed across multiple stations along a user defined route, and then averaged over a user defined reliability weeks.

PORTAL provides four travel time reliability calculations of 95%, 80%, 20%, and 5%. A 95% reliability time refers to ranked travel time within the 95th percentile, which is equivalent to being late once a month. An 80% reliability time is equivalent to being late once a week. A reliability of 20% is equivalent to XXX. And a reliability of 5% travel time is equivalent to free-flow.

_Average Travel Time_
The average travel time is the same as travel time calculated at the 50 percentile over the user selected reliability weeks.

_Sample Count_
Data used to calculate travel time on freeways comes from readings taken every 20 seconds from loop detectors. Data used to calculate travel times from arterials generally comes from bluetooth detectors and taken each time a car is detected, suggesting travel times along arterials might be less precise due to this method. Sample counts show the number of samples used to calculate travel time for each week. Travel time calculated with sample counts less or equal to 30 (and indicated with a red color) is less than ideal. Travel time calculated with sample counts great than 30 and less than 50 is acceptable. And travel times calculated with sample counts greater than 50 is best. There is also an option to see the average sample count for all four weeks.

_Download_

### Plotting Options
_Standard_
The Standard plot shows detailed travel time for each day per week. Users can zoom in on a specific time frame on the plot by clicking at the start date of interest and drag to the end date of interest (Figure X).

_Aggregate_
The Aggregate plot shows hourly average travel time per hour aggregated by user-specified days of the week per week. For example, Figure X shows average travel time (y-axis) per hour (x-axis) per week aggregated by Tuesday, Wednesday, and Thursday.

_Yearly_
The Yearly plot shows hourly average travel time per hour aggregated by user-specified days of the week per year. Figure X shows hourly average travel time per hour aggregated by Tuesday, Wednesday, and Thursday, per year.

_Zoom in/out_
For higher resolution data visualization, select a period of time on the plot by clicking and dragging the cursor. Click the "reset zoom" button revert back to the original plot.
