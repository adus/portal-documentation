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
| delay         | Vehicle Hours Traveled, minus the time it would take a vehicle to travel at the maximum permitted speed on a segment | Float     | 0.01      |
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

| Name                | Description                                                    | Type                           | Example                   |
| ------------------- | -------------------------------------------------------------- | ------------------------------ | ------------------------- |
| average_travel_time | Average travel time of segment in minutes                      | Float                          | 151.4                     |
| countreadings       | Sample Size                                                    | Integer                        | 5                         |
| id                  | Unique ID value of aggregation                                 | Integer                        | 2386933463                |
| resolution          | Temporal Resolution of Data                                    | Time Formatted String          | 00:05:00                  |    
| segment_id          | Unique ID, used to join with segment inventory metadata        | Integer                        | 2264                      |
| starttime           | Start time of chosen resolution                                | Date and Time Formatted String | 2019-07-10T00:00:00-07:00 |

### Raw travel time
The following data are provided:

| Name                               | Description                                                    | Type                           | Example                          |
| ---------------------------------- | -------------------------------------------------------------- | ------------------------------ | -------------------------------- |
| below_min_filter                   |                                                                | Integer                        | 0                                |
| calc_confidence_interval           |                                                                | Float                          | 47.62680841791146                |
| calc_variance                      |                                                                | Float                          | 1910.7777233115469               |
| exceeded_max_filter                |                                                                | Integer                        | 0                                |
| segment_calc_time                  |                                                                | Date and Time Formatted String | 2019-07-15T08:10:13.870000-07:00 |
| segment_id                         |                                                                | Integer                        | 2264                             |
| segment_travel_time                |                                                                | Integer                        | 250                              |
| std_deviation_calc_samples_removed |                                                                | Integer                        | 3                                |
| std_deviation_filter_value         |                                                                | Float                          | 625.985307791092                 |


### Travel time segment inventory
The following data are provided:

| Name                          | Description                                                    | Type    | Example                             |
| ----------------------------- | -------------------------------------------------------------- | ------- | ----------------------------------- |
| active                        | Indicator of whether the segment is active in the system       | Boolean | true                                |
| beginning_dcu                 | ID value for DCU at start of segment                           | Integer | 535                                 |
| calculation_period            |                                                                | Integer | 10                                  |
| calculation_threshold         |                                                                | Integer | 30                                  |
| end_dcu                       | ID value for DCU at end of segment                             | Integer | 533                                 |
| minimum_lanes_reporting       | If beginning_dcu and end_dcu are present, this is a null value. Otherwise, it is 0.5 | Float             | 0.5 |
| minimum_samples               | Minimum number of samples required to produce a data point     | Integer | 3                                   |
| segment_id                    | Unique ID of Highway Segment                                   | Integer | 2667                                |
| segment_length                | Length of segment, as measured between beginning and end DCUs  | Integer | 100                                 |
| segment_maximum_filter        |                                                                | Integer | 1000                                |
| segment_minimum_filter        |                                                                | Integer | 10                                  |
| segment_name                  | Name of Segment                                                | String  | Powell Blvd EB at SE 8th to SE 33rd |
| segment_type                  |                                                                | Integer | 1                                   |
| source_system                 |                                                                | String  | TravelTime                          |
| standard_deviation_multiplier |                                                                | Float   | 1.65                                |
| standard_deviation_samples    |                                                                | Integer | 30                                  |
| station_id                    | Agency given name or ID value, null if none issued             | Integer | null                                |
| use_standard_deviation_filter |                                                                | Boolean | true                                |

### Travel time DCU inventory
The following data are provided:

| Name                               | Description                                                     | Type    | Example                |
| ---------------------------------- | --------------------------------------------------------------- | ------- | ---------------------- |
| active                             | Indicator of whether the detector is active in the system       | Boolean | true                   |
| location_type                      | Intersection or free flowing traffic                            | String  | Intersection           |
| dcu_id                             | Unique ID value; if preceded by ```-```, if location_type is Free Flowing Traffic. | Integer | 556 |
| dcu_name                           | Name of intersection, if location_type is intersection. Numeric, matching dcu_id, with name appended if free flowing traffic | String | SW Beaverton Hillsdale Hwy at SW Capitol Hwy |
| geom.type                          | Always Point, allowing for coordinate values.                   | String  | Point                  |
| geom.coordinates.0                 | The longitude of the Point specifying the DCU                   | Float   | -122.69778             |
| geom.coordinates.1                 | The latitude of the Point specifying the DCU                    | Float   | 45.47809               |
| longitude                          | The longitude of the Point specifying the DCU                   | Float   | -122.69778             |
| latitude                           | The latitude of the Point specifying the DCU                    | Float   | 45.47809               |
| highway                            | Name of highway on which the detector is situated               | String  | B-H                    |
| roadway_number                     |                                                                 | Integer | 1                      |
| milepoint                          | Null for free flowing traffic. Float value for intersections    | Float   | 0.0                    |
| owner                              | Agency name                                                     | String  | City of Portland       |

</p>
</details>

<details><summary>Other Download Categories</summary>
<p>

### Aggregated CLS
The following data are provided:

| Name                               | Description                                                        | Type                           | Example                   |
| ---------------------------------- | ------------------------------------------------------------------ | ------------------------------ | ------------------------- |
| aggregated_records                 | Number of records sampled to created each data point               | Integer                        | 104                       |
| bin_count                          | Count of vehicles by classification bin                            | Integer                        | 0                         |
| bin_type                           | Description of classification bin - either length or speed         | String                         | length                    |
| bin_number                         | Classification bin number. These Classifications can be seen in the next table | Integer            | 4                         |
| bin_resolution                     | Temporal resolution for data - 15 minutes, 1 hour, or 1 day        | Time Formatted String          | 01:00:00                  |
| bin_time                           | The timestamp for the data value, to a granularity of 20 seconds   | Date and Time Formatted String | 2019-07-10T00:00:00-07:00 |
| id                                 | The record id value used by the API framework                      | Integer                        | 938253264                 |
| lane                               | Lane in which the data was collected. Lane 1 is the left most lane | Integer                        | 3                         |
| stationid                          | Unique id value of the collection station; corresponds to the agencyid in the stations metadata | Integer     | 54              |


Bin Number Classifications:

|Bin Number | Vehicle Length |
|-----------|----------------|
|        1  |      0-20 ft.  |
|        2  |     20-35 ft.  |
|        3  |     35-60 ft.  |
|        4  |    60-120 ft.  |

More information about Vehicle Length data can be seen [_here._]({{ site.url }}{{ site.baseurl }}/documents/freight/)

### Voyage Volume
The following data are provided:

| Name                               | Description                                                        | Type                           | Example                   |
| ---------------------------------- | ------------------------------------------------------------------ | ------------------------------ | ------------------------- |
| controller_id                      |                                                                    | Integer                        | 4258                      |
| logtime                            |                                                                    | Date and Time Formatted String | 2017-01-03T00:07:00-08:00 |
| period                             |                                                                    | Integer                        | 15                        |
| detector_1_volume                  |                                                                    | Integer                        | 0                         |
| detector_2_volume                  |                                                                    | Integer                        | 0                         |
| detector_3_volume                  |                                                                    | Integer                        | 0                         |
| detector_4_volume                  |                                                                    | Integer                        | 0                         |
| detector_5_volume                  |                                                                    | Integer                        | 5                         |
| detector_6_volume                  |                                                                    | Integer                        | 3                         |
| detector_7_volume                  |                                                                    | Integer                        | 0                         |
| detector_8_volume                  |                                                                    | Integer                        | 0                         |
| detector_9_volume                  |                                                                    | Integer                        | 4                         |
| detector_10_volume                 |                                                                    | Integer                        | 4                         |
| detector_11_volume                 |                                                                    | Integer                        | 0                         |
| detector_12_volume                 |                                                                    | Integer                        | 0                         |
| detector_13_volume                 |                                                                    | Integer                        | 0                         |
| detector_14_volume                 |                                                                    | Integer                        | 0                         |
| detector_15_volume                 |                                                                    | Integer                        | 0                         |
| detector_16_volume                 |                                                                    | Integer                        | 0                         |
| detector_17_volume                 |                                                                    | Integer                        | 0                         |
| detector_18_volume                 |                                                                    | Integer                        | 0                         |
| detector_19_volume                 |                                                                    | Integer                        | 1                         |
| detector_20_volume                 |                                                                    | Integer                        | 1                         |
| detector_21_volume                 |                                                                    | Integer                        | 1                         |
| detector_22_volume                 |                                                                    | Integer                        | 0                         |
| detector_23_volume                 |                                                                    | Integer                        | 0                         |
| detector_24_volume                 |                                                                    | Integer                        | 2                         |
| detector_25_volume                 |                                                                    | Integer                        | 3                         |
| detector_26_volume                 |                                                                    | Integer                        | 0                         |
| detector_27_volume                 |                                                                    | Integer                        | 0                         |
| detector_28_volume                 |                                                                    | Integer                        | 0                         |
| detector_29_volume                 |                                                                    | Integer                        | 0                         |
| detector_30_volume                 |                                                                    | Integer                        | 0                         |
| detector_31_volume                 |                                                                    | Integer                        | 0                         |
| detector_32_volume                 |                                                                    | Integer                        | 0                         |

### Transit Quarterly Data
The data is returned as a Zipped CSV file.  The data provided in the CSV file are as follows.

| Name                               | Description                                                            | Type                           | Example                   |
| ---------------------------------- | ---------------------------------------------------------------------- | ------------------------------ | ------------------------- |
| summary_begin_date                 | The start date of the fiscal quarter requested                         | Date and Time Formatted String | 02DEC2018:00:00:00        |
| route_number                       | Trimet bus route number                                                | Integer                        | 2                         |
| direction                          | 0 if departing from initial origin, 1 if departing from route endpoint | Integer                        | 0                         |
| service_key                        |                                                                        | String                         | S                         |
| stop                               | Number of stops made on route                                          | Integer                        | 100                       |
| location_id                        |                                                                        | Integer                        | 9301                      |
| ons                                | Number of riders embarking                                             | Integer                        | 121                       |
| offs                               | Number of riders disembarking                                          | Integer                        | 2                         |
| total                              | Aggregate of ons and offs                                              | Integer                        | 123                       |
| estimated_load                     |                                                                        | Integer                        | 175                       |
| cumulative_ons                     | Aggregate of ons over route history                                    | Integer                        | 176                       |
| cumulative_offs                    | Aggregate of offs over route history                                   | Integer                        | 2                         |
| lifts                              | Lift usages as a percentage of all stops                               | Float                          | 0.6818181818              |

</p>
</details>



Last updated: 2020-08-11
