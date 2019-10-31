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

### Raw travel time

### Travel time segment inventory

### Travel time DCU inventory

### Aggregated CLS

### Voyage Volume

Last updated: 2018-09-20
