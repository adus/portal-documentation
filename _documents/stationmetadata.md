---
title: "Station Metadata"
---
The _/highways/api/stationmetadata_ endpoint returns station data for each individual station in the network. This information can be constrained within a date range through the use of the `start_date` and `end_date` parameters.

This endpoint returns data in JSON format by default. An overview of the data returned by this endpoint, including attribute descriptions, can be found on the Downloads page, in the [_Stations Metadata_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) section of the Highway Data dropdown menu on the downloads page.

## Parameters
Stations Metadata takes the following Parameters

| Name         | Required | Description                                        | Type              | Example      |
| ------------ | -------- | -------------------------------------------------- | ----------------- | ------------ |
|  start_date  | No       | Beginning Date for Data Query                      | YYYY-MM-DD String | 2020-05-10   |
|  end_date    | No       | End Date for Data Query in                         | YYYY-MM-DD String | 2020-05-16   |
|  format      | No       | File format. Acceptable values are CSV or JSON     | String            | CSV          |

## Example Request
```http://new.portal.its.pdx.edu:8080/highways/api/stationmetadata/?start_date=2020-05-10&end_date=2020-05-16&format=csv```

## Example Response (CSV)
```
stationid,highwayid,milepost,locationtext,length,numberlanes,agencyid,x_coord,y_coord,active_dates
5208,55,36.15,Salmon CR SB,,,205es03616:_MS,-122.640267,45.71191,"{""lower"": ""2017-04-06"", ""upper"": null, ""bounds"": ""[)""}"
3154,10,0.25,Wilshire (2DS043) @ SB OR 217 MP0.25,0.185,,321,-122.78043,45.50622,"{""lower"": ""2014-04-29"", ""upper"": null, ""bounds"": ""[)""}"
10522,610,304.4,Alberta HOV (2R003) to NB I-5,0.62,,388,-122.67814,45.56172,"{""lower"": ""2017-12-04"", ""upper"": null, ""bounds"": ""[)""}"
10285,608,6.7,102nd off-ramp (2DS020) @ EB I-84 MP6.7,31.745,,285,-122.55889,45.54448,"{""lower"": ""2015-11-12"", ""upper"": null, ""bounds"": ""[)""}"
10358,608,5.82,Halsey off-ramp (2DS019) @ EB I-84 MP5.82,0.94,,358,-122.5659,45.53213,"{""lower"": ""2015-11-12"", ""upper"": null, ""bounds"": ""[)""}"
1010,1,295.18,Capitol (2R306) to NB I-5,1.26,,157,-122.72042,45.45293,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1004,1,289.63,WB Nyberg Slip (2R312) to NB I-5,0.57,,383,-122.7511,45.38279,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1011,1,296.26,Spring Garden (2R305) to NB I-5,0.71,,158,-122.69942,45.46213,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1008,1,293.18,Haines (2R308) to NB I-5,0.78,,155,-122.7431,45.43495,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1007,1,292.18,OR 217/Kruse Way (2R317) to NB I-5,0.785,,83,-122.74224,45.42213,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1009,1,293.74,99W (2R307) to NB I-5,1.0,,156,-122.74179,45.4429,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1039,2,290.4,Lower Boones (2R321) to SB I-5,0.935,,86,-122.74824,45.39565,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
1075,10,4.35,Scholls Ferry (2R332) to SB OR 217,0.805,,18,-122.7847,45.45004,"{""lower"": ""2012-03-01"", ""upper"": null, ""bounds"": ""[)""}"
```

Last Updated: 2020-09-02
