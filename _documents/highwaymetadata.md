---
title: "Highway Metadata"
---
The _/highways/api/highwaymetadata_ end point returns highway data for each highway in the network, sorted by station number. By default, the data will be returned by this
endpoint will be in JSON format.

## Parameters
Detector Metadata takes the following Parameters

| Name         | Required | Description                                        | Type   | Example      |
| ------------ | -------- | -------------------------------------------------- | ------ | ------------ |
|  format      | No       | File format. Acceptable values are CSV or JSON     | String | CSV          |

## Example Request
```http://new.portal.its.pdx.edu:8080/highways/api/detectormetadata/?format=csv```

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
