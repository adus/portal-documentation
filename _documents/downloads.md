---
title: "Downloads"
---
In addition to being able to download data from each page in PORTAL, the _Downloads_ page provides the opportunity to download data over longer time frames over multiple locations.

## Learning objectives
By the end of the tutorial users should be able to:

* Understand the parameters of each download option for each section
* Know what data is being downloaded (e.g. variables and units)

### Highways
Highway data can be downloaded from this section by selecting the start and end date of interest, days of week, format, highway of interest, and temporal resolution. Multiple highway sections can be downloaded by holding the ctrl key and clicking on the desired highway.

The following data are provided:
- starttime: start time
- resolution: temporal resolution of frequency of data collected
- detector_id: detector id along selected route
- speed: average speed of vehicles traveling per hour that pass the detector
- volume: number of vehicles per hour that pass the detector
- occupancy: percent of time cars are being detected
- countreadings:
- delay: vht minus the time it would take a vehicle to travel at the maximum permitted speed on a segment.
- traveltime: the average amount of time spent traveling within a segment.
- vht: (vehicle hours traveled) total hours traveled within a segment by - all vehicles
- vmt: (vehicle miles traveled) total miles traveled on a segment by all vehicles

To get distance traveled divide vmt by volume.

### [Stations metadata]

The following data are provided:
- stationid: station ID
- highwayid: highway ID
- milepost: milepost (mi)
- locationtext: agency provided location information
- length: length of segment (mi)
- numberlanes: number of lanes at the station
- agencyid: ID of the agency maintaining the station
- x_coord: longitude
- y_coord: latitude
- active_dates: active date of station

To [_Stations_]({{ site.url }}{{ site.baseurl }}/documents/stations/)

### Detector metadata

The following data are provided:
- detectorid: unique detector id, used to join with raw or aggregated data
- stationid: unique station id, used to join with stations metadata
- highwayid: unique highway id, used to join with highways metadata
- milepost: milepost (mi)
- detectortitle: agency given name or id for detector
- lanenumber: PORTAL lane number, where lane 1 is the left most lane regardless of agency jurisdiction
- agency_lane: agency given lane number where lane 1 is left most lane for ODOT, and lane 1 is right most lane for WSDOT
- active_dates: active date of detector

To [_Stations_]({{ site.url }}{{ site.baseurl }}/documents/stations/)

### Highways metadata
The following data are provided:
- highwayid: unique highway id
- direction: direction of flow
- highwayname: name of highway
- oppositehighwayid: id of highway of opposite flow

### Aggregated travel time
The following data are provided:
- average_travel_time: average travel time of segment (min)
- countreadings: sample size
- id:
- resolution: either one hour or five minutes
- segment_id: unique id, used to join with travel time segment inventory metadata
- starttime: start time of chosen resolution

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
- active: true or false
- dcu_id:
- dcu_name:
- geom.coordinates.0: longitude
- geom.cooridnates.1: latitude
- geom.type:
- highway: highway name
- latitude: latitude
- location_type: intersection or free flowing traffic
- longitude: longitude
- milepoint:
- owner: agency name
- roadway_number:

### Aggregated CLS
The following data are provided:
- aggregated_records:
- bin_count:
- bin_number:
- bin_resolution: 15 minutes, one hour, one day
- bin_time:
- bin_type:
- id:
- lane: lane 1 is the right most lane
- stationid: unique station id, to be used with stations metadata

### Voyage Volume

Last updated: 2019-10-31
