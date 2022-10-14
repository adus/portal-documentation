---
title: "Segment Inventory"
---
The _/traveltime/api/seginventory_ end point returns segment data for each segment in the network.

This endpoint returns data in JSON format by default. An overview of the data returned by this endpoint, including attribute descriptions, can be found on the Downloads page, in the [_Travel Time Segment Inventory_]({{ site.url }}{{ site.baseurl }}/documents/downloads/) section of the Travel Time Data dropdown menu on the downloads page.


## Parameters
Detector Metadata takes the following Parameters

| Name         | Required  | Description                                        | Type   | Example      |
| ------------ | --------- | -------------------------------------------------- | ------ | ------------ |
|  format      | No        | File format. Acceptable values are CSV or JSON     | String | CSV          |

## Example Request
```https://new.portal.its.pdx.edu/traveltime/api/seginventory?format=csv```

## Example Response (CSV)
```
active,beginning_dcu,calculation_period,calculation_threshold,end_dcu,minimum_lanes_reporting,minimum_samples,segment_id,segment_length,segment_maximum_filter,segment_minimum_filter,segment_name,segment_type,source_system,standard_deviation_multiplier,standard_deviation_samples,station_id,use_standard_deviation_filter
True,535,10,30,533,,3,2667,100,1000,10,Powell Blvd EB at SE 8th to SE 33rd,1,TravelTime,1.65,30,,True
True,533,10,30,535,,3,2668,100,1000,10,Powell Blvd WB at SE 33rd to SE 8th,1,TravelTime,1.65,30,,True
True,507,10,30,511,,3,2427,8712,1188,99,Baseline Rd WB at 185th Ave to Cornelius Pass Rd,1,TravelTime,1.65,50,,True
True,470,10,60,471,,6,2299,5805,792,79,McDonald to Durham,1,TravelTime,1.65,60,,True
True,525,10,30,526,,3,2418,45936,5911,422,US26 EB at Arlie Mitchell Rd to Government Camp Loop West,1,TravelTime,1.65,30,,False
True,543,10,30,536,,3,2522,100,600,10,Milwaukie Ave NB at SE Pershing to Powell EB at SE 21st,1,TravelTime,1.65,30,,True
True,541,10,30,535,,3,2513,100,600,10,McLoughlin Blvd NB at SE 17th to Powell Blvd EB at SE 8th,1,TravelTime,1.65,30,,True
True,,2,30,,0.5,3,2387,3960,2700,36,SR 14 WB MP2.40 @ Blandford,2,,1.96,15,014es00240:_MW_Stn,True
True,524,10,30,523,,3,2410,2429,331,27,TV Hwy at Cedar Hills Blvd to Lombard Ave,1,TravelTime,1.65,50,,True
True,530,10,30,531,,3,2479,100,600,10,Barbur Blvd NB at Capitol to Bertha,1,TravelTime,1.65,30,,True
True,518,10,30,519,,3,2417,2587,352,29,Scholls Ferry Rd at OR217 SB to Hall Blvd,1,TravelTime,1.65,50,,True
True,506,10,40,505,,3,2439,16949,2311,192,185th Ave NB at TV Hwy to US26,1,TravelTime,1.65,40,,True
True,534,10,30,557,,3,2523,100,600,10,SE 82nd Ave SB at Foster to Springwater Corridor Trail,1,TravelTime,1.65,30,,True
True,,2,30,,0.5,3,2357,4118,2808,37,I-205 NB MP28.36 @ Mill Plain,2,,1.96,15,205es02836:_MN_Stn,True
True,468,10,60,467,,6,2294,5122,698,70,OR217 to I-5,1,TravelTime,1.65,60,,True
True,,2,30,,0.5,3,2281,4594,3132,48,I-205 ORE 99E SB,2,DAC,1.96,15,235,True
True,532,10,30,531,,3,2478,100,600,10,Barbur Blvd SB at Hamilton to Bertha,1,TravelTime,1.65,30,,True
True,546,10,30,535,,3,2512,100,600,10,Holgate Blvd WB at SE 17th to Powell WB at SE 8th,1,TravelTime,1.65,30,,True
True,499,15,60,498,,6,2454,14467,3600,60,Construction Zone NB DC,1,TravelTime,1.65,20,,True
```
Last Updated: 2020-09-02
