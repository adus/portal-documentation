---
title: "Download Quarterly Data"
---
This call will return a quarterly Trimet ridership report.  The data is returned as a zipped CSV; no alternative formats are available via the API call.

An overview of the data returned by this endpoint, including attribute descriptions, can be found on the Downloads page, in the [_Transit Quarterly Data_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) section of the Other Download Categories dropdown menu on the downloads page.

## Parameters
Voyage Volume takes the following Parameters

| Name         | Required  | Description | Type   | Example        |
| ------------ | --------- | ----------- | ------ | -------------- |
| agency       | Yes       | Agency Name | String | trimet         |
| quarter      | Yes       | Period      | String | 2019-q2-spring |


The only valid value for the `agency` parameter is TriMet.

Valid values for the `quarter` parameter conform to the pattern: `YYYY-q1-winter`, `YYYY-q2-spring`, `YYYY-q3-summer`, or `YYYY-q4-fall`.

## Example Request
```http://new.portal.its.pdx.edu:8080/transit/downloadquarterlydata?agency=trimet&quarter=2019-q3-summer```

Last Updated: 2020-09-02
