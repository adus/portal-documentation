---
title: "Voyage Volume"
---
The _/arterial/api/voyagevolume_ endpoint returns a set of traffic volume data for Portland, Oregon. The returned data is grouped by its `controller_id` attribute and broken up by system detector count within that grouping. Due to the quantity of data in the database, API calls to this endpoint must be constrained within a date range through the use of the `start_date` and `end_date` parameters in order to reliably return any data.

This endpoint returns data in JSON format by default.

## Parameters
Voyage Volume takes the following Parameters

| Name         | Required | Description                                        | Type              | Example      |
| ------------ | -------- | -------------------------------------------------- | ----------------- | ------------ |
|  start_date  | Yes      | Beginning Date for Data Query                      | YYYY-MM-DD String | 2020-05-10   |
|  end_date    | Yes      | End Date for Data Query in                         | YYYY-MM-DD String | 2020-05-16   |
|  format      | No       | File format. Acceptable values are CSV or JSON     | String            | CSV          |

## Example Request
```http://new.portal.its.pdx.edu:8080/arterial/api/voyagevolume/?start_date=2020-05-10&end_date=2020-05-16&format=csv```

## Example Response (CSV)
```
controller_id,detector_10_volume,detector_11_volume,detector_12_volume,detector_13_volume,detector_14_volume,detector_15_volume,detector_16_volume,detector_17_volume,detector_18_volume,detector_19_volume,detector_1_volume,detector_20_volume,detector_21_volume,detector_22_volume,detector_23_volume,detector_24_volume,detector_25_volume,detector_26_volume,detector_27_volume,detector_28_volume,detector_29_volume,detector_2_volume,detector_30_volume,detector_31_volume,detector_32_volume,detector_3_volume,detector_4_volume,detector_5_volume,detector_6_volume,detector_7_volume,detector_8_volume,detector_9_volume,logtime,period
4258,4,0,0,0,0,0,0,0,0,1,0,1,1,0,0,2,3,0,0,0,0,0,0,0,0,0,0,5,3,0,0,4,2017-01-03T00:07:00-08:00,15
2158,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2017-01-03T00:07:00-08:00,15
8531,0,6,6,0,1,0,2,0,0,0,0,0,18,14,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2017-01-03T00:07:00-08:00,15
1088,5,0,0,1,4,1,0,0,0,6,1,6,7,0,0,0,0,0,0,0,0,2,0,0,0,1,1,0,0,0,0,5,2017-01-03T00:07:00-08:00,15
6001,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2017-01-03T00:07:00-08:00,15
8403,10,16,0,0,0,0,0,0,0,2,11,19,31,0,0,1,2,12,11,0,0,0,0,0,0,0,0,1,2,0,0,7,2017-01-03T00:07:00-08:00,15
5810,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2017-01-03T00:07:00-08:00,15
8402,4,9,0,0,7,0,3,12,0,19,4,2,20,0,0,6,2,0,0,0,0,0,0,0,0,0,0,0,0,0,0,5,2017-01-03T00:07:00-08:00,15
8584,15,0,0,0,1,0,0,0,0,14,0,15,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,14,2017-01-03T00:07:00-08:00,15
3087,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2017-01-03T00:07:00-08:00,15
8586,9,0,0,10,0,0,0,0,0,16,0,17,0,0,17,0,2,0,0,0,0,0,0,0,0,0,0,0,0,0,0,10,2017-01-03T00:07:00-08:00,15
2133,0,0,0,0,1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2,0,0,0,0,2017-01-03T00:07:00-08:00,15
1029,14,14,0,0,4,4,0,0,4,6,2,6,6,0,0,5,5,0,0,5,0,4,0,1,2,2,3,1,1,6,1,13,2017-01-03T00:07:00-08:00,15
4055,10,29,29,1,0,0,0,0,5,3,0,3,22,23,4,1,3,1,1,0,0,4,0,0,0,4,4,0,0,4,0,10,2017-01-03T00:07:00-08:00,15
5059,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,2017-01-03T00:07:00-08:00,15
8703,0,3,4,0,11,0,0,0,0,0,0,0,12,0,0,7,0,0,0,0,0,0,0,0,0,4,0,1,0,0,0,0,2017-01-03T00:07:00-08:00,15
1027,12,13,0,0,0,0,0,0,0,8,1,8,8,0,0,2,3,0,0,0,0,2,0,0,0,0,0,12,3,0,0,12,2017-01-03T00:07:00-08:00,15
8473,0,0,4,0,0,0,0,0,0,8,0,7,0,15,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,4,2017-01-03T00:07:00-08:00,15
8471,11,0,0,0,0,0,1,0,0,12,0,12,0,0,0,0,0,2,0,0,0,0,0,0,0,0,0,3,0,0,0,4,2017-01-03T00:07:00-08:00,15
```
