---
title: "Detector Metadata"
---
The _/highways/api/detectormetadata_ end point returns station data for each individual detector in the network, sorted by station number. This information can be constrained to a date or a range of dates using the start_date and end_date parameters, which will return only stations active within that range of dates. This endpoint returns data in JSON format by default.

## Parameters
Detector Metadata takes the following Parameters

| Name         | Required | Description                                    | Type              | Example      |
| ------------ | -------- | ---------------------------------------------- | ----------------- | ------------ |
|  start_date  | No       | Beginning Date for Data Query                  | YYYY-MM-DD String | 2020-05-10   |
|  end_date    | No       | End Date for Data Query in                     | YYYY-MM-DD string | 2020-05-16   |
|  format      | No       | File format. Acceptable values are CSV or JSON | String            | CSV          |

## Example Request
```http://new.portal.its.pdx.edu:8080/highways/api/detectormetadata/?start_date=2020-05-10&end_date=2020-05-16&format=csv```

## Example Response (CSV)
```
detectorid,stationid,highwayid,milepost,detectortitle,lanenumber,agency_lane,active_dates
102017,5207,54,36.15,205es03615:_MN___1,1,1,"{""lower"": ""2017-04-06"", ""upper"": null, ""bounds"": ""[)""}"
102018,5207,54,36.15,205es03615:_MN___2,2,2,"{""lower"": ""2017-04-06"", ""upper"": null, ""bounds"": ""[)""}"
102019,5208,55,36.15,205es03616:_MS___1,1,1,"{""lower"": ""2017-04-06"", ""upper"": null, ""bounds"": ""[)""}"
102020,5208,55,36.15,205es03616:_MS___2,2,2,"{""lower"": ""2017-04-06"", ""upper"": null, ""bounds"": ""[)""}"
101766,10347,612,0.0,101766,2,5,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101767,10347,612,0.0,101767,1,6,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101976,10330,612,0.0,101976,2,5,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101977,10330,612,0.0,101977,1,6,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101982,10331,612,0.0,101982,2,5,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101983,10331,612,0.0,101983,1,6,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101694,10326,612,0.0,101694,4,3,"{""lower"": ""2015-11-04"", ""upper"": null, ""bounds"": ""[)""}"
101709,10328,612,0.0,101709,1,6,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101714,10329,612,0.0,101714,2,5,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101715,10329,612,0.0,101715,1,6,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
101732,10332,612,0.0,101732,2,5,"{""lower"": null, ""upper"": null, ""bounds"": ""()""}"
100836,1147,2,306.6,100836,3,1,"{""lower"": ""2015-06-16"", ""upper"": null, ""bounds"": ""[)""}"
101769,10349,607,57.52,101769,1,1,"{""lower"": ""2015-09-16"", ""upper"": null, ""bounds"": ""[)""}"
101762,10347,612,0.0,101762,6,1,"{""lower"": ""2015-09-16"", ""upper"": null, ""bounds"": ""[)""}"
101763,10347,612,0.0,101763,5,2,"{""lower"": ""2015-09-16"", ""upper"": null, ""bounds"": ""[)""}"
```
