---
title: "Aggregated Bin Data"
---
The _/freight/api/aggregatedbindata_ endpoint returns records of vehicle length, sorted into one of four bins.  For more information on bin lengths, see [_Aggregated CLS_]({{ site.url }}{{ site.baseurl }}/documents/downloads) in the 'Other Download Categories' dropdown list on the downloads page.  The stationid parameter corresponds to the station ids, which can be returned from the [_Stations Metadata_]({{ site.url }}{{ site.baseurl }}/documents/stationsmetadata) endpoint.

## Parameters
Aggregated Bin Data Data takes the following Parameters:

| Name          | Required  | Description                                        | Type               | Example      |
| ------------- | --------- | -------------------------------------------------- | ------------------ | ------------ |
| start_date    | No        | Beginning Date for results                         | YYYY-MM-DD String  | 2020-08-11   |
| end_date      | No        | End Date for results                               | YYYY-MM-DD String  | 2020-08-11   |
| format        | No        | File format. Acceptable values are CSV or JSON     | String             | CSV          |
| stationid     | No        | integer value of station ID                        | Integer            | 54           |
| resolution    | No        | URL encoded time value used to divide data points  | URL Encoded String | 00%3A15%3A00 |

## Example Request
```http://new.portal.its.pdx.edu:8080/freight/api/aggregatedbindata?start_date=2019-07-10&end_date=2019-07-11&stationid=54&format=csv```

## Example Response (CSV)
```
aggregated_records,bin_count,bin_number,bin_resolution,bin_time,bin_type,id,lane,stationid
104,0,4,01:00:00,2019-07-10T00:00:00-07:00,length,938253264,3,54
104,34,1,01:00:00,2019-07-10T00:00:00-07:00,length,938253307,3,54
104,0,3,01:00:00,2019-07-10T00:00:00-07:00,length,938253382,3,54
104,1,3,01:00:00,2019-07-10T00:00:00-07:00,length,938253554,1,54
104,6,2,01:00:00,2019-07-10T00:00:00-07:00,length,938253555,2,54
104,0,4,01:00:00,2019-07-10T00:00:00-07:00,length,938253655,1,54
104,19,1,01:00:00,2019-07-10T00:00:00-07:00,length,938253803,1,54
28,5,1,00:15:00,2019-07-10T00:00:00-07:00,length,938253933,1,54
104,2,3,01:00:00,2019-07-10T00:00:00-07:00,length,938253959,2,54
104,3,2,01:00:00,2019-07-10T00:00:00-07:00,length,938253963,1,54
104,148,1,01:00:00,2019-07-10T00:00:00-07:00,length,938254090,2,54
104,2,4,01:00:00,2019-07-10T00:00:00-07:00,length,938254222,2,54
104,1,2,01:00:00,2019-07-10T00:00:00-07:00,length,938254562,3,54
28,0,4,00:15:00,2019-07-10T00:00:00-07:00,length,938254571,1,54
28,1,3,00:15:00,2019-07-10T00:00:00-07:00,length,938254707,1,54
28,1,2,00:15:00,2019-07-10T00:00:00-07:00,length,938254708,2,54
28,0,3,00:15:00,2019-07-10T00:00:00-07:00,length,938255005,3,54
28,13,1,00:15:00,2019-07-10T00:00:00-07:00,length,938255056,3,54
28,0,4,00:15:00,2019-07-10T00:00:00-07:00,length,938255095,3,54
```