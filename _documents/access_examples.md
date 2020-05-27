---
title: "API Access Examples"
---
The _API Access Examples_ page offers some insight into accessing the API using various common methods. What follows here is a simple
code repository which provides a basic framework for how to interface with the API.

## Learning objectives
By the end of the tutorial users should be able to:

* Understand how to access the API using cURL and Python

<details><summary>cURL Request examples</summary>
<p>
The versatility of cURL makes it straightforward to download PORTAL data from the command line. However, each form on the Downloads page, e.g. Highways, Detector Metadata, Aggregated TravelTime Data, etc., has a unique combination of fields to be filled.  Some basic access examples to facilitate easier cURL access will be provided below.

#### Curl Example \#1 - Highways Data, Single Day
```
curl 'http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/?start_date=2020-05-11&end_date=2020-05-11&format=
csv&highway_id=3&highway_id=54&resolution=00%3A15%3A00' -H 'Host: new.portal.its.pdx.edu:8080' -H 'Referer:
http://new.portal.its.pdx.edu:8080/downloads/ -o highways_data.csv'
```

This sample query on the Highways dataset returns CSV formatted data with a 15 minute resolution for the highways with ID values 3 and 54 (I-205 NB, and I-205 NB Washington) for May 11, 2020.  It then saves that data into a csv file using -o.

#### Curl Example \#2 - Highways Data, Limited by Days of Week Over a Range of Dates
```
curl "http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/?start_date=2020-05-04&end_date=2020-05-15&
days_of_week=1&days_of_week=2&days_of_week=3&days_of_week=4&days_of_week=5&days_of_week=6&days_of_week=7&format=csv&
highway_id=3&highway_id=54&resolution=01"%"3A00"%"3A00" -H 'Host: new.portal.its.pdx.edu:8080' -H 'Referer: 
http://new.portal.its.pdx.edu:8080/downloads/ -o highways_data.csv'
```

This sample query on the Highways dataset returns CSV formatted data with a 15 minute resolution for the highways with ID values 3 and 51 (I-205 NB and I-205 NB Washington) for Wednesdays, Thursdays and Fridays only, within a date range of May 05, 2020 and May 15, 2020.

#### Curl Example \#3 - Travel Time Data
```
curl "http://new.portal.its.pdx.edu:8080/traveltime/api/aggregatedsegmentcalcs/?start_date=2020-05-27
&end_date=2020-0527&format=csv&resolution=01"%"3A00"%"3A00&segment_id=2264&segment_id=2275" -H 'Host:
new.portal.its.pdx.edu:8080' -H 'Referer: http://new.portal.its.pdx.edu:8080/downloads/ -o travel_time_data.csv'
```

This sample query on the Travel Time dataset returns CSV formatted data with a 1 hour resolution, for the I-205 Foster NB and SB segments. 

#### Curl Example \#4 - Trimet Data
```
curl "http://new.portal.its.pdx.edu:8080/transit/downloadquarterlydata?agency=trimet&quarter=2019-q3-summer"
-H 'Host: new.portal.its.pdx.edu:8080' -H 'Referer: http://new.portal.its.pdx.edu:8080/downloads/ -o trimet_data.zip'
```

This query on the TriMet ridership dataset returns the TriMet for the selected quarter; zip is selected here as that is how the file is served through the website - when unzipped, the data is available in .csv format _only_.
</p>
</details>

<details><summary>Python Request examples</summary>
<p>
Python methods will go here.
</p>
</details>

<details><summary>Query-Specific Fields</summary>
<p>
This section will be a list tables of values specific to each query - ie, a list of highways by Hwy # in the Highways dataset, to facilitate ease of use.
</p>
</details>
