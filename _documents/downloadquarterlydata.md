---
title: "Download Quarterly Data"
---
This call will return a quarterly Trimet ridership report.  The data is returned as a zipped CSV; no alternative formats are available via the API call.

The only valid value for the `agency` parameter is TriMet.

Valid values for the `quarter` parameter conform to the pattern: `YYYY-q1-winter`, `YYYY-q2-spring`, `YYYY-q3-summer`, or `YYYY-q4-fall`.

The only

| Name         | Required  | Description | Type                  | Example          |
| ------------ | --------- | ----------- | --------------------- | ---------------- |
| agency       | Yes       | Agency Name | Date formatted string | 2020-08-11       |
| quarter      | Yes       | Period      | String                | 2019-q2-spring   |


## Example Request
```http://new.portal.its.pdx.edu:8080/transit/downloadquarterlydata?agency=trimet&quarter=2019-q3-summer```
