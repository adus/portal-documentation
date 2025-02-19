---
title: "Highway Metadata"
---
The _/highways/api/highwaymetadata_ endpoint returns highway data for each highway in the network, sorted by station number.

This endpoint returns data in JSON format by default. An overview of the data returned by this endpoint, including attribute descriptions, can be found on the Downloads page, in the [_Highways Metadata_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) section of the Highway Data dropdown menu on the Downloads page.

## Parameters
Detector Metadata takes the following Parameters

| Name         | Required | Description                                        | Type   | Example      |
| ------------ | -------- | -------------------------------------------------- | ------ | ------------ |
|  format      | No       | File format. Acceptable values are `csv` or `json`     | String | `csv`          |

## Example Request
```https://new.portal.its.pdx.edu/highways/api/highwaymetadata/?format=csv```

## Example Response (CSV)
```
highwayid,direction,highwayname,oppositehighwayid
614,WEST,R5 I-84,
0,unkn,n/a,
615,EAST,R5 I-84,
16,SOUTH,US 99E,
61,SOUTH,SR 7,
65,SOUTH,SR 97,
69,SOUTH,SR 101,
71,SOUTH,SR 103,
73,SOUTH,SR 105,
77,SOUTH,SR 123,
79,SOUTH,SR 131,
81,SOUTH,SR 141,
85,SOUTH,SR 197,
87,SOUTH,SR 401,
89,SOUTH,SR 409,
91,SOUTH,SR 411,
95,SOUTH,SR 433,
97,SOUTH,SR 501,
101,SOUTH,SR 503,
```

Last Updated: 2020-09-02
