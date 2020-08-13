---
title: "Aggregated Segment Calcs"
---
The aggregatedsegmentcalcs endpoint returns aggregated travel time and count readings for one or more segments for a specified date or range of dates. A segment is defined as a route between a set of starting coordinates and a set of ending coordinates. The segment or segments retutned are specified using the segment_id parameter, which takes an integer. The valid segment IDs can be found by making a call to the [_seginventory_]({{ site.url }}{{ site.baseurl }}/documents/seginventory/) endpoint.
<br /> <br />
Valid resolutions for this endpoint are 5 minutes and 1 hour. The default resolution, if not specified, is 5 minutes.

## Parameters
Aggregated Segment Calcs takes the following parameters:

| Name         | Required  | Description                                                            | Type                  | Example      |
| ------------ | --------- | ---------------------------------------------------------------------- | --------------------- | ------------ |
| start_date   | No        | Beginning Date for Data Query in YYYY-MM-DD                            | Date formatted string | 2019-07-10   |
| end_date     | No        | End Date for Data Query in YYYY-MM-DD Format                           | Date formatted string | 2019-07-16   |
| format       | Yes       | File format. Acceptable values are CSV or JSON                         | String                | CSV          |
| resolution   | No        | URL encoded time value used to divide data points                      | URL Encoded String    | 00%3A15%3A00 |
| segment_id   | No        | The ID value of a segment.                                             | Integer               | 2264         |

## Example Request
```http://new.portal.its.pdx.edu:8080/traveltime/api/aggregatedsegmentcalcs/?start_date=2019-07-10&end_date=2019-07-16&segment_id=2264&format=csv```

## Example Response (CSV)
```
average_travel_time,countreadings,id,resolution,segment_id,starttime
151.4,5,2386933463,00:05:00,2264,2019-07-10T00:00:00-07:00
193.0,5,2386948761,00:05:00,2264,2019-07-10T00:05:00-07:00
117.0,5,2386965097,00:05:00,2264,2019-07-10T00:10:00-07:00
363.3541666666667,48,2386979938,01:00:00,2264,2019-07-10T00:00:00-07:00
377.75,4,2386980876,00:05:00,2264,2019-07-10T00:15:00-07:00
497.4,5,2386998453,00:05:00,2264,2019-07-10T00:20:00-07:00
430.6,5,2387014322,00:05:00,2264,2019-07-10T00:25:00-07:00
497.4,5,2387029732,00:05:00,2264,2019-07-10T00:30:00-07:00
430.6,5,2387046085,00:05:00,2264,2019-07-10T00:35:00-07:00
497.4,5,2387061759,00:05:00,2264,2019-07-10T00:40:00-07:00
464.0,4,2387077588,00:05:00,2264,2019-07-10T00:45:00-07:00
,0,2387093010,00:05:00,2264,2019-07-10T00:50:00-07:00
,0,2387109509,00:05:00,2264,2019-07-10T00:55:00-07:00
,0,2387124091,00:05:00,2264,2019-07-10T01:00:00-07:00
,0,2387140945,00:05:00,2264,2019-07-10T01:05:00-07:00
,0,2387156688,00:05:00,2264,2019-07-10T01:10:00-07:00
,0,2387172004,01:00:00,2264,2019-07-10T01:00:00-07:00
,0,2387172848,00:05:00,2264,2019-07-10T01:15:00-07:00
,0,2387190397,00:05:00,2264,2019-07-10T01:20:00-07:00
```
