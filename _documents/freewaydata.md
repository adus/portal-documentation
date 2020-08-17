---
title: "Freeway Data"
---
The _/highways/api/freewaydata_ endpoint returns information about one or more freeways. This information can be constrained to a date or a range of dates using the `start_date` and `end_date` parameters. The freeway is specified using the `highway_id` parameter, which takes in integer. A list of valid highway IDs can be obtained by making a call to [_highway metadata_]({{ site.url }}{{ site.baseurl }}/documents/highwaymetadata/).

Due to the quantity of data available, API calls to this endpoint must be constrained within a date range through the use of the `start_date` and `end_date` parameters in order to reliably return any data.

Valid resolutions for this endpoint are 20 seconds, 5 minutes, 15 minutes, 1 hour, and 1 day. If not specified, the default resolution is 1 hour.

This endpoint returns data in JSON format by default.
## Parameters
Freeway Data takes the following Parameters

| Name         | Required | Description                                                            | Type                  | Example      |
| ------------ | -------- | ---------------------------------------------------------------------- | --------------------- | ------------ |
| start_date   | Yes      | Beginning Date for Data Query                                          | YYYY-MM-DD String     | 2020-08-11   |
| end_date     | Yes      | End Date for Data Query                                                | YYYY-MM-DD String     | 2020-08-11   |
| days_of_week | No       | Filter results by day of week. Sunday = 1, Saturday = 7                | Integer               | 1            |
| highway_id   | No       | Integer value of any given highway ID                                  | Integer               | 54           |
| resolution   | No       | URL encoded time value used to divide data points                      | URL Encoded String    | 00%3A15%3A00 |
| format       | No       | File format. Acceptable values are CSV or JSON                         | String                | CSV          |

## Example Request
```http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/?start_date=2020-05-10&end_date=2020-05-16&days_of_week=2&days_of_week=5&highway_id=3&format=csv```

## Example Response (CSV)
```
starttime,resolution,detector_id,speed,volume,occupancy,countreadings,delay,traveltime,vht,vmt
2020-05-11T00:00:00-07:00,01:00:00,100907,59.0,16,0.88,28,0.01,0.4,0.11,6.24
2020-05-11T00:00:00-07:00,01:00:00,101069,54.92,94,1.09,180,0.04,0.45,0.7,38.54
2020-05-11T00:00:00-07:00,01:00:00,102254,63.49,194,1.44,180,-0.04,0.75,2.43,154.23
2020-05-11T00:00:00-07:00,01:00:00,100925,55.53,59,0.54,94,0.1,1.39,1.37,75.82
2020-05-11T00:00:00-07:00,01:00:00,101985,64.69,147,1.03,145,-0.05,0.7,1.72,110.99
2020-05-11T00:00:00-07:00,01:00:00,102238,63.68,107,0.67,180,-0.05,0.85,1.51,96.3
2020-05-11T00:00:00-07:00,01:00:00,101074,62.22,245,2.11,179,-0.03,0.76,3.11,193.55
2020-05-11T00:00:00-07:00,01:00:00,102316,61.44,138,1.27,180,-0.02,0.79,1.82,111.78
2020-05-11T00:00:00-07:00,01:00:00,100935,,0,0.0,3,,,,0.0
2020-05-11T00:00:00-07:00,01:00:00,100922,60.78,119,0.99,180,-0.02,1.32,2.61,158.87

```

Last Updated: 2020-08-17
