---
title: "Downloads"
---
In addition to being able to download data from each page in PORTAL, the _Downloads_ page provides the opportunity to download data over longer time frames, multiple locations, or both.

## Learning objectives
By the end of the tutorial users should be able to:

* Understand the parameters of each download option for each section
* Know what data is being downloaded (e.g. variables and units)

<details><summary>Highways Data</summary>
<p>

### Highways
Highway data can be downloaded from this section by selecting the start and end date of interest, days of week, format, highway of interest, and temporal resolution. Multiple highway sections can be downloaded by holding the ctrl key and clicking on the desired highway.

The following data are provided:
- starttime: Start time of the data.
- resolution: Temporal resolution of frequency of data.
- detector_id: Detector id along selected route.
- speed: Average speed of vehicles traveling per hour that pass the detector.
- volume: Number of vehicles per hour that pass the detector.
- occupancy: Percentage of time cars are being detected.
- countreadings:
- delay: VHT minus the time it would take a vehicle to travel at the maximum permitted speed on a segment.
- traveltime: The average amount of time for vehicles to travel through a segment.
- vht: (vehicle hours traveled) Total hours traveled within a segment by all vehicles.
- vmt: (vehicle miles traveled) Total miles traveled on a segment by all vehicles.

Distance traveled can be calculated by dividing vmt by volume.

A tutorial on using the Highways function can be found [_here_]({{ site.url }}{{ site.baseurl }}/documents/highways/).

### Stations metadata

The following data are provided:
- stationid: Station ID.
- highwayid: Highway ID.
- milepost: Milepost (mi).
- locationtext: Agency provided location information.
- length: Length of segment in miles.
- numberlanes: Number of lanes at the station.
- agencyid: ID of the agency maintaining the station.
- x_coord: Longitude of station.
- y_coord: Latitude.
- active_dates: Initial active date of station.

An interactive map of all the stations in the network can be viewed [_here_]({{ site.url }}{{ site.baseurl }}/documents/stations/)

### Detector metadata

The following data are provided:
- detectorid: Unique detector id, used to join with raw or aggregated data.
- stationid: Unique station id, used to join with stations metadata.
- highwayid: Unique highway id, used to join with highways metadata.
- milepost: Milepost (mi).
- detectortitle: Agency given name or id for detector.
- lanenumber: PORTAL lane number, where lane 1 is the left most lane regardless of agency jurisdiction.
- agency_lane: Agency given lane number where lane 1 is left most lane for ODOT, and lane 1 is right most lane for WSDOT.
- active_dates: Initial active date of detector.

An interactive map of all the stations in the network can be viewed here [_here_]({{ site.url }}{{ site.baseurl }}/documents/stations/)

### Highways metadata
The following data are provided:
- highwayid: Unique highway id.
- direction: Direction of flow.
- highwayname: Name of highway.
- oppositehighwayid: Id of highway with opposite flow.

</p>
</details>

<details><summary>Travel Time Data</summary>
<p>

### Aggregated travel time
The following data are provided:
- average_travel_time: Average travel time of segment in minutes.
- countreadings: Sample size.
- id:
- resolution: Temporal resolution of data - either one hour or five minutes.
- segment_id: Unique id, used to join with travel time segment inventory metadata.
- starttime: Start time of chosen resolution.

### Raw travel time
The following data are provided:
- below_min_filter:
- calc_confidence_interval
- calc_variance:
- exceeded_max_filter:
- segment_calc_time:
- segment_id:
- segment_travel_time:
- std_deviation_calc_samples_removed:
- std_deviation_filter_value:

### Travel time segment inventory
The following data are provided:
- active: true or false
- beginning_dcu:
- calculation_period:
- calculation_threshold:
- end_dcu:
- minimum_lanes_reporting:
- minimum_samples:
- segment_id:
- segment_length:
- segment_maximum_filter:
- segment_minimum_filter:
- segment_name:
- segment_type:
- source_system:
- standard_deviation_multiplier:
- standard_deviation_samples:
- station_id:
- use_standard_deviation_filter:

### Travel time DCU inventory
The following data are provided:
- active: True or False.
- dcu_id: Unique id value; preceded by ```-``` if location_type is free flowing traffic.
- dcu_name: Name of intersection, if location_type is Intersection. Eg. Foster Rd at SE 82nd.\
            Numeric, matching dcu_id value without leading ```-``` if location type is free flowing traffic.
- geom.type: This data field is always "Point", for geom.coordinates.
- geom.coordinates.0: Longitude
- geom.coordinates.1: Latitude.
- highway: Highway Name.
- latitude: Latitude.
- location_type: Intersection or free flowing traffic, dependant on location.
- longitude: Longitude.
- milepoint: Null for free flowing traffic.  Float value for intersections.
- owner: Agency name.
- roadway_number:
</p>
</details>

<details><summary>Other Download Categories</summary>
<p>

### Aggregated CLS
The following data are provided:
- aggregated_records: Number of records sampled to create individual data point.
- bin_count: Count of vehicles by classification bin.
- bin_type: Description of classification bin - either length or speed.
- bin_number: Classification bin number.  These classifications can be seen in the table below this section.
- bin_resolution: Temporal Resolution - 15 minutes, one hour, or one day.
- bin_time: The timestamp of the data value, to a granularity of 20 seconds.
- id: The record id value used by the API framework (Django).
- lane: Lane in which the data was collected. Lane 1 is the left most lane.
- stationid: Unique id of the collection station, which corresponds to the agencyid in the stations metadata.

Bin Number Classifications:

|Bin Number | Vehicle Length |
|-----------|----------------|
|        1  |      0-20 ft.  |
|        2  |     20-35 ft.  |
|        3  |     35-60 ft.  |
|        4  |    60-120 ft.  |

More information about Vehicle Length data can be seen [_here._]({{ site.url }}{{ site.baseurl }}/documents/freight/)

### Voyage Volume

### Transit Quarterly Data
</p>
</details>



Last updated: 2020-07-07
