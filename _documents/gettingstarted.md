---
title: "Getting Started with the Portal API"
---

The Portal API offers a publicly available means of accessing the data in the Portal archive;
and no token required in order to make a request.

The base URL for the API is:
<br />

`http://new.portal.its.pdx.edu:8080/{endpoint}`
<br /><br />

The following endpoints may be appended to the base URL, in order to access data from specific datasets:
<br />

| endpoint                               | description                                         |
|--------------------------------------- | --------------------------------------------------- |
| /highways/api/freewaydata              | Highway speed and volume data                       |
| /highways/api/stationsmetadata         | Highway station metadata                            |
| /highways/api/detectormetadata         | Highway detector metadata                           |
| /highways/api/highwaymetadata          | Highway metadata                                    |
| /traveltime/api/aggregatedsegmentcalcs | Travel times along highways by segment              |
| /traveltime/api/segmentcalc            | Raw travel time data                                |
| /traveltime/api/seginventory           | List of segments for travel time calculations       | 
| /traveltime/api/dcuinventory           | Bluetooth Data Collection Unit metadata             |
| /freight/api/aggregatedbindata         | Freight data based on vehicle length metrics        |
| /arterial/api/voyagevolume             | Traffic volume data for arterial routes in Portland |
| /transit/downloadquarterlydata         | Download zipped Trimet data for specified quarter   |\

\
 As no token is required for access to the API, a very simple cURL header can be used in order to access this data:

| Header |  Usage  |
| ------ | ------- |
| curl {base URL}/{endpoint}/{query parameters} -H 'Host:new.portal.its.pdx.edu:8080' | Request a dataset from the specified endpoint with the specified query parameters. |

Most endpoints serve data in JSON format by default. Currently, the only exception to this is the Trimet Quarterly Transit Data, which is only served as a zip file containing CSV formatted data. For all other endpoints, CSV formatted data is available by request by specifying the `format=csv` parameter. 

Some examples of API calls made with cURL and Python have been provided on the [_API access examples_]({{ site.url }}{{ site.baseurl }}/documents/access_examples/) page.

All data accessible via the API is also served from the API to the portal website; visiting the tutorial pages for [_Vehicle Length (Freight)_]({{ site.url }}{{ site.baseurl }}/documents/freight/), [_Highways_]({{ site.url }}{{ site.baseurl }}/documents/highways/), [_Stations_]({{ site.url }}{{ site.baseurl }}/documents/stations/), and [_Travel Time_]({{ site.url }}{{ site.baseurl }}/documents/travel-time/) in the Portal Website Documentation section can provide some crucial insight into the data to a new user.

Additionally, many of the data attributes for each dataset are listed on the [_Downloads_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) page. The parameters for each individual API endpoint are clearly defined on the page for that endpoint.  Additionally, it's important to note that the metadata available through the ```/highways/api/stationsmetadata```, ```/highways/api/detectormetadata ```, ```/highways/api/highwaymetadata```, and ```/traveltime/api/seginventory``` endpoints is crucial to the success of making API calls for specific locations, as it contains mappings between the real locations of those objects and the unique id values which are referenced in data returned by calls to other endpoints.  This metadata is downloadable both through API calls, or via manual download from the [_Downloads_](http://new.portal.its.pdx.edu:8080/downloads/) page on the PORTAL website.

Last Edited 08-19-20
