---
title: "Download Quarterly Data"
---
This call will return a quarterly Trimet ridership report, as a zipped CSV file.  As of right now, only two quarters are available; the quarter
values which are currently available are 2019-q2-spring, and 2019-q3-summer.  The only valid agency, currently, is TriMet.

| Name         | Required  | Description                                   | Type                  | Example          |
| ------------ | --------- | --------------------------------------------- | --------------------- | ---------------- |
| agency       | Yes       | The only valid option is trimet               | Date formatted string | 2020-08-11       |
| quarter      | Yes       | String, formatted similarly to 2019-q3-summer | String                | 2019-q2-spring   |


## Example Request
```http://new.portal.its.pdx.edu:8080/transit/downloadquarterlydata?agency=trimet&quarter=2019-q3-summer```
