---
title: "Raw Travel Time"
---
The _/traveltime/api/segmentcalc_ endpoint returns all the individual (non-aggregated) travel time calculations in one ore more segments (each of which is defined as a route between a set of starting coordinates and a set of ending coordinates). The segment or segments returned are specified by passing the `segment_id` parameter, which takes an integer. The valid segment IDs for this endpoint can be found in the data returned by a call to the [_seginventory_]({{ site.url }}{{ site.baseurl }}/documents/seginventory/) endpoint.

Due to the quantity of data available, API calls to this endpoint must be constrained within a date range through the use of the `start_date` and `end_date` parameters in order to reliably return any data.

This endpoint returns data in JSON format by default. An overview of the data returned by this endpoint, including attribute descriptions, can be found on the Downloads page, in the [_Raw Travel Time_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) section of the Travel Time Data dropdown menu on the downloads page.

## Parameters
Segment Calc takes the following parameters:

| Name         | Required  | Description                                      | Type                  | Example      |
| ------------ | --------- | ------------------------------------------------ | --------------------- | ------------ |
| start_date   | Yes       | Beginning Date for Data Query in YYYY-MM-DD      | Date formatted String | 2019-07-10   |
| end_date     | Yes       | End Date for Data Query in YYYY-MM-DD Format     | Date formatted String | 2019-07-16   |
| segment_id   | No        | The ID value of a segment.                       | Integer               | 2264         |
| format       | No        | File format. Acceptable values are CSV or JSON   | String                | CSV          |

## Example Request
```https://new.portal.its.pdx.edu/traveltime/api/segmentcalc/?start_date=2019-07-10&end_date=2019-07-16&segment_id=2264&format=csv```

## Example Response (CSV)
```
below_min_filter,calc_confidence_interval,calc_variance,exceeded_max_filter,segment_calc_time,segment_id,segment_travel_time,std_deviation_calc_samples_removed,std_deviation_filter_value
0,47.62680841791146,1910.7777233115469,0,2019-07-15T08:10:13.870000-07:00,2264,250,3,625.985307791092
,,,,2019-07-12T02:43:56.443000-07:00,2264,,,
0,27.739097824477074,691.0682950191571,0,2019-07-14T17:26:19.290000-07:00,2264,201,11,292.14712922602826
,,,,2019-07-14T05:04:04.793000-07:00,2264,,,
0,91.84276125908704,7419.019478573576,0,2019-07-12T13:06:05.013000-07:00,2264,431,13,606.9405957187217
0,15.783286044384685,211.38965221124943,0,2019-07-14T19:19:17.543000-07:00,2264,179,17,344.9302539780056
0,63.20044260842664,2894.638962569994,0,2019-07-15T08:02:13.523000-07:00,2264,226,8,453.90285676718827
0,137.05280600966222,12216.124908424914,0,2019-07-15T05:44:09.357000-07:00,2264,258,15,1043.6730441916566
0,83.25856385808284,5495.865588090551,0,2019-07-14T11:27:12.090000-07:00,2264,218,8,392.93832389982845
0,8.267695402107005,63.50800894854586,0,2019-07-14T12:13:12.767000-07:00,2264,198,21,283.2372606427088
,,,,2019-07-10T01:29:55.590000-07:00,2264,,,
0,131.00863258199135,12757.024089635885,0,2019-07-10T09:42:05.257000-07:00,2264,548,1,919.07907964233
0,37.14847914988638,1341.9923240241667,0,2019-07-10T14:44:10.550000-07:00,2264,237,11,624.2426675933058
0,62.78188228464351,3222.6333564654096,0,2019-07-15T07:45:13.357000-07:00,2264,241,4,507.1922615249074
6,838.6053438099856,313628.88184663624,0,2019-07-14T08:29:10.347000-07:00,2264,513,18,1494.1113118110252
0,134.99541910594726,10384.705685618726,0,2019-07-10T06:03:02.050000-07:00,2264,243,6,741.0110109265383
14,404.9355648242871,21328.457142857143,0,2019-07-14T07:26:07.273000-07:00,2264,1276,39,1650.9809597497995
,,,,2019-07-10T02:07:56.993000-07:00,2264,,,
0,252.93178070425998,22982.808529945556,0,2019-07-10T15:44:10.437000-07:00,2264,687,10,868.6713802022657
```
Last Updated: 2022-10-13
