---
title: "Getting Started with the Portal API"
---

The portal API offers a means of accessing the data in the ADUS archive; it is
publicly available, with no token required in order to make a request.  _{If there
is a limit on the number of requests which can be made in a particular period of time,
those limits should be noted here}_.

The base URL for the API is:

http://new.portal.its.pdx.edu:8080/<span>{endpoint}</span>

The following endpoints may be appended to the base URL, in order to access data from specific datasets:
| endpoint | description |
|--------- | ----------- |
| /highways/api/freewaydata | Highway speed and volume data |
| /highways/api/stationsmetadata | Highway station metadata |
| /highways/api/detectormetadata | Highway detector metadata |
| /highways/api/highwaymetadata | Highway metadata |
| /traveltime/api/aggregatedsegmentcalcs | Travel times along specific segments of highway |
| /traveltime/api/segmentcalc | Raw travel time data |
| /traveltime/api/seginventory | List of segment for travel time calculations | 
| /traveltime/api/dcuinventory |  |
| /freight/api/aggregatedbindata |  Freight data based on vehicle length metrics |
| /arterial/api/voyagevolume |  |
| /transit/downloadquarterlydata | Download zipped Trimet data for specified quarter |

As no token is required for access to the API, a very simple cURL header can be used in order to access
this data:

| Header |  Usage  |
| ------ | ------- |
| curl {base URL}/{endpoint}/{query parameters} -H 'Host:new.portal.its.pdx.edu:8080' | Request a dataset from the specified endpoint with the specified query parameters. |

Portal data is served in CSV format by default; json is available by request for _most_ data sets by specifying ```format=json``` in the request.  

