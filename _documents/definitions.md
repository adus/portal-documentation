---
title: "Definitions"
---

This file contains definitions of the key quantities/metrics used in the PORTAL web site and related general information. 
This page is not complete at the moment, please contact the PORTAL team if the definition you need or information 
you want is not on this page.

_**Stations Page: Speed:**_  Volume-weighted average speed in MPH at that detector for the selected time period. 

_**Stations Page: Volume (VPLPH):**_  Volume of vehicles passing by this location expressed as Vehicles per Lane per Hour. 
This metric scales data to an hour no matter what resolution is selected. In addition, this metric averages over lanes, 
so the result is always a per lane, per hour figure. 

_**Stations Page: Average Volume:**_ This metric calculates the total total volume of vehicles recorded by the selected detector(s) during the time resolution selected and averages the volume for that time period over the days selected. 
For example, if 5 min resolution is selected and  a one day time range is selected, this metric will provide 
the volume during each 5 minute period during that day. If a multiple day time range is selected, the metric will 
provide the average volume over those days for each 5 minute time period during the day. This metric does not 
scale to an hour and does not average over lanes.
Note: May need a new name. Suggestions welcome.

_**Stations Page: Occupancy:**_  Average detector occupancy; percentage between 0 and 100. Reflects the percentage of time the detector was occupied; that is the percentage of time a vehicle was positioned over the detector. 

_**Stations Page: VMT:**_  Vehicle Miles Travelled (VMT) for the selected detector during the selected time period. VMT is calculated using the influence area (see below) of a detector and the volume observed at that detector during the selected time period. VMT is calculated as (volume)x(influence_area). 

_**Stations Page: VHT:**_  Vehicle Hours Travelled (VHT) for the selected detector during the selected time period. VHT is calculated using the influence area (see below) of a detector, the volume observed at that detector during the selected time period and the average speed at that detector during the selected time period. VHT is calculated as (volume)x(influence_area/speed))
 
_**Stations Page: Travel Time:**_ Travel time in minutes observed for the influence area (see below) of the detector during the selected time period. Travel time is calculated as (influence_area)/(speed). 

_**Stations Page: Delay:**_ The delay in minutes observed at the detector for the selected time period. Delay is calculated using the influence area (see below) of the detector and the observed average speed at the detector. Delay assumes 60 mph as the free flow speed. Delay is calculated as ((influence_area/speed)-(influence_area/free_flow_speed));

_**Travel Time Page: Travel Time**_ The travel times reported on the Travel Time Page are taken from multiple data sources. Freeway travel times are calculated based on point speeds observed at loop and radar detectors. Travel time for an individual detector is calculated using the influence area of a detector (defined below) and the speed observed at that detector as described in the calculation for the Travel Time for the Stations page above. Arterial travel time is calculated by matching readings from bluetooth devices deployed along the arterial. To get the travel time for a set of segments, the travel times for the individual (small) segments are summed.
      
_**General: Influence Area**_
The influence area of a detector is calculated using the midpoint method. That is the influence area of a detector is the region that lies between the midpoint between the detector and the nearest upstream detector and the midpoint between the detector and the the hearest downstream detector.

_**General: FHWA Documentation**_  
Documentation produced for the Multi Modal Data Set Clean-up for Portland Oregon Metropolitan Region project done for FHWA in 2012. The document is dated, but still contains valuable information. 
[FHWA Documentation](https://portal.its.pdx.edu/static/files/fhwa/Freeway%20Data%20Documentation.pdf)

Last Changed 09-08-2020
