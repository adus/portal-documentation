---
title: "Data Collection Unit Inventory"
---
The _/traveltime/api/dcuinventory_ endpoint returns data collection unit information for each unit in the network.

This endpoint returns data in JSON format by default. An overview of the data returned by this endpoint, including attribute descriptions, can be found on the Downloads page, in the [_Travel Time DCU Inventory_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) section of the Travel Time DCU Inventory dropdown menu on the Downloads page.


## Parameters
Detector Metadata takes the following Parameters

| Name         | Required  | Description                                        | Type   | Example      |
| ------------ | --------- | -------------------------------------------------- | ------ | ------------ |
|  format      | No        | File format. Acceptable values are `csv` or `json`     | String | `csv`          |

## Example Request
```https://new.portal.its.pdx.edu/traveltime/api/dcuinventory?format=csv```

## Example Response (CSV)
```
active,dcu_id,dcu_name,geom.coordinates.0,geom.coordinates.1,geom.type,highway,latitude,location_type,longitude,milepoint,owner,roadway_number
True,556,SW Beaverton Hillsdale Hwy at SW Capitol Hwy,-122.69778,45.47809,Point,B-H,45.47809,Intersection,-122.69778,0.0,City of Portland,1
True,505,185th Ave at US26 EB,-122.86752,45.54088,Point,185th,45.54088,Intersection,0.0,0.0,Wash Co,1
True,539,Powell Blvd at SE 42nd 43rd,-122.619,45.4975,Point,US26,45.4975,Intersection,-122.619,0.0,City of Portland,1
True,537,Powell Blvd at SE 78th,-122.5838,45.4974,Point,US26,45.4974,Intersection,-122.5838,0.0,City of Portland,1
True,474,Barnes Rd WB @ VMS,-122.77266,45.50901,Point,OR217,45.50901,Intersection,0.0,0.0,ODOT,1
True,538,Powell Blvd at SE 54th,-122.6071,45.4975,Point,US26,45.4975,Intersection,-122.6071,0.0,City of Portland,1
True,528,OR35 at US26 MP57.52,-121.71418,45.28302,Point,US26,45.28302,FreeFlowingTraffic,0.0,57.52,ODOT,1
True,493,US101 at 22nd St,-124.00779,44.98159,Point,US101,44.98159,Intersection,-124.00779,113.82,ODOT,1
True,475,B-H CN2 @ VMS,-122.79204,45.48868,Point,OR217,45.48868,Intersection,0.0,0.0,ODOT,1
True,530,Barbur Blvd at Capitol,-122.72106,45.45366,Point,99W,45.45366,Intersection,-122.72106,1.12,City of Portland,1
True,483,Kruse Way WB @ Kruse Oaks VMS,-122.73919,45.41936,Point,OR217,45.41936,Intersection,0.0,0.0,ODOT,1
True,510,Cornelius Pass Rd at TV Hwy,-122.90217,45.49746,Point,CPR,45.49746,Intersection,0.0,0.0,Wash Co,1
True,504,I-5 @ SR14 (WA),-122.67064,45.6238,Point,I-5,45.6238,Intersection,0.0,0.0,ODOT,1
True,492,US101 at Neotsu Dr,-123.98687,45.00171,Point,US101,45.00171,Intersection,-123.98687,111.78,ODOT,1
True,480,72nd NB Loop Ramp,-122.75095,45.42632,Point,OR217,45.42632,Intersection,0.0,0.0,ODOT,1
True,535,Powell Blvd at SE 8th,-122.65785,45.5015,Point,US26,45.5015,Intersection,-122.65785,0.0,City of Portland,1
True,529,US26 at Frog Lake MP57.52,-121.70026,45.22827,Point,US26,45.22827,FreeFlowingTraffic,0.0,57.52,ODOT,1
True,555,SW Macadam Ave at SW Bancroft St,-122.67298,45.49319,Point,Macad,45.49319,Intersection,-122.67298,0.0,City of Portland,1
True,524,TV Hwy at Cedar Hills Blvd,-122.8108,45.48825,Point,TVH,45.48825,Intersection,0.0,0.0,Wash Co,1
```

Last Updated: 2025-02-19
