---
title: "Downloads"
---
In addition to being able to download data from each page in PORTAL, the [_Downloads_](http://new.portal.its.pdx.edu:8080/downloads/) page provides the opportunity to download data over longer time frames, multiple locations, or both.  The data available through the downloads page is the same as is available through the API.

## Learning objectives
By the end of the tutorial users should be able to:

* Understand the parameters of each download option for each section
* Know what data is being downloaded (e.g. variables and units)

<details><summary>Highways Data</summary>
<p>

### Highways
Highway data can be downloaded from this section by selecting the start and end date of interest, days of week, format, highway of interest, and temporal resolution. Multiple highway sections can be downloaded at once by holding the ctrl key and clicking on the desired highway in the Highway menu.

The following data are provided:

| Name          | Description                                                                         | Type                       | Example                   |
| ------------- | ----------------------------------------------------------------------------------- | -------------------------- | ------------------------- |
| starttime     | Starting time of the data                                                           | Date/Time Formatted String | 2020-05-11T00:00:00-07:00 |
| resolution    | Temporal Resolution of the data                                                     | Time Formatted String      | 01:00:00                  |
| detector_id   | Detector ID along selected route                                                    | Integer                    | 100907                    |
| speed         | Average speed of vehicles passing the detector                                      | Float                      | 59.0                      |
| volume        | Number of vehicles per hour which pass the detector                                 | Integer                    | 16                        |
| occupancy     | Percentage of time cars are being detected                                          | Float                      | .88                       |
| countreadings |                                                                                     | Integer                    | 28                        |
| delay         | Vehicle Hours Traveled, minus the time it would take a vehicle to travel at the maximum permitted speed on a segment | Float | 0.01          |
| traveltime    | The average amount of time for a vehicle to travel through a segment                | Float                      | 0.4                       |
| vht           | Vehicle Hours Traveled - the total hours traveled within a segment by all vehicles  | Float                      | 0.11                      |
| vmt           | Vehicle Miles Traveled - the total miles traveled on a segment by all vehicles      | Float                      | 6.24                      |

In order to calculate distance traveled, divide `vmt` by `volume`.

A tutorial on using the Highways function can be found [_here_]({{ site.url }}{{ site.baseurl }}/documents/highways/).

### Stations metadata
Information on the individual stations in the network can be downloaded from this section; the `highwayid` attribute is used to join these values to Highways and Highway Metadata. The `stationid` attribute can be used to join these values to Detector Metadata.

The following data are provided:

| Name         | Description                                                                         | Type    | Example                              |
| ------------ | ----------------------------------------------------------------------------- | ------- | ------------------------------------ |
| stationid    | The unique station ID value of each station                                   | Integer | 3154                                 |
| highwayid    | The unique highway ID value of the highway on which the station is located    | Integer | 10                                   |
| milepost     | The mile post location of the station on the highway                          | Float   | 0.25                                 |
| locationtext | Description of the location of the station                                    | String  | Wilshire (2DS043) @ SB OR 217 MP0.25 |
| length       | Length of segment in miles                                                    | Float   | 0.185                                |
| numberlanes  | Number of lanes at the station - returned as an empty value in _most_ queries | Integer | (Null)                               |
| agencyid     | Station ID issued by agency maintaining the station                           | Integer | 321                                  |
| x_coord      | Longitude of station                                                          | Float   | -122.78043                           |
| y_coord      | Latitude of station                                                           | Float   | 45.50622                             |
| active_dates | Provided as a set of key: value pairs; lower indicates the initial active date of the station, upper indicates the date the station was deactivated | String | {""lower"": ""2014-04-29"", ""upper"": null, ""bounds"": ""[)""} |

An interactive map of all the stations in the network can be viewed [_here_]({{ site.url }}{{ site.baseurl }}/documents/stations/)

### Detector metadata
Information on the individual detectors at each station can be downloaded from this section; the `highwayid` attribute is used to join these values to Highways and Highway Metadata. The `stationid` attribute can be used to join these values to Detector Metadata.

The following data are provided:

| Name          | Description                                                                            | Type              | Example              |
| ------------- | -------------------------------------------------------------------------------------- | ----------------- | ---------------------|
| detectorid    | The unique detector ID value of each detector                                          | Integer           | 102017               |
| stationid     | The unique station ID of the station at which the detector is located                  | Integer           | 5207                 |
| highwayid     | The unique highway ID value of the highway on which the detector is located            | Integer           | 54                   |
| milepost      | The mile post location of the station on the highway                                   | Float             | 36.15                |
| detectortitle | Agency given name (if any), or repeat of id value                                      | String or Integer | 205es03615:\_MN___1  |
| lanenumber    | PORTAL lane number; 1 is the leftmost lane, regardless of agency jurisdiction          | Integer           | 1                    |
| agency_lane   | Agency issued lane number, where 1 is leftmost lane for ODOT, rightmost lane for WSDOT | Integer           | 1                    |
| active_dates  | Provided as a set of key: value pairs; lower indicates the initial active date of the station, upper indicates the date the station was deactivated | String | {""lower"": ""2017-04-06"", ""upper"": null, ""bounds"": ""[)""} |

An interactive map of all the stations in the network can be viewed [_here_]({{ site.url }}{{ site.baseurl }}/documents/stations/)

### Highways metadata
Information on the highways in the system can be downloaded from this section.

The following data are provided:

| Name              | Description                                                    | Type    | Example         |
| ----------------- | -------------------------------------------------------------- | ------- | ----------------|
| highwayid         | The unique ID value of each highway                            | Integer | 616             |
| direction         | Cardinal direction of traffic flow (or CONST for construction) | String  | EAST            |
| highwayname       | Name of Highway                                                | String  | R2 Beltline Hwy |
| oppositehighwayid | ID of highway with opposite flow (or null value, if none)      | Integer | 617             |


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
- beginning_dcu: id value for DCU start point; see 'Travel time DCU inventory' below for further details.
- calculation_period:
- calculation_threshold:
- end_dcu: id value for DCU end point; see 'Travel time DCU inventory' below for further details.
- minimum_lanes_reporting:
- minimum_samples:
- segment_id: 
- segment_length: Length of segment between beginning and ending DCUs.
- segment_maximum_filter:
- segment_minimum_filter:
- segment_name: Name of segment.
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



Last updated: 2020-08-11
