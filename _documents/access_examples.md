---
title: "API Access Examples"
---
The _API Access Examples_ page offers some insight into accessing the API using various common methods. What follows here is a simple
code repository which provides a basic framework for how to interface with the API.

## Learning objectives
By the end of the tutorial users should be able to:

* Understand how to fill the fields involved in making a request to the database.
* Understand how to access the API using cURL and Python.

Each of the forms on the downloads page has a set of fields which may be filled in order to request a constrained set of data. The purpose of some of these fields, such as start_date and end_date should be self-explanatory.  The individual values for other, less-intuitive fields, such as the station_id, highway_id or segment_id fields are available through the Stations Metadata, Highways Metadata, or Travel Time Segment Inventory forms, all of which only require start and end dates as input.

The date format used by the forms is YYYY-MM-DD.

<details><summary>Sample cURL Requests</summary>

<p>
The versatility of cURL makes it straightforward to download PORTAL data from the command line.  Some basic access examples to facilitate easier cURL access are provided below.

#### Curl Example \#1 - Highways Data, Single Day

The following sample query on the Highways dataset returns CSV formatted data with a 15 minute resolution for the highways with ID values 3 and 54 (I-205 NB, and I-205 NB Washington) for May 11, 2020.  It then saves that data into a csv file using -o.

```
curl 'http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/?start_date=2020-05-11&end_date=2020-05-11&
format=csv&highway_id=3&highway_id=54&resolution=00%3A15%3A00' -H 'Host: new.portal.its.pdx.edu:8080' -H 'Referer:
http://new.portal.its.pdx.edu:8080/downloads/ -o highways_data.csv'
```

#### Curl Example \#2 - Highways Data, Limited by Days of Week Over a Range of Dates

The following sample query on the Highways dataset returns CSV formatted data with a 15 minute resolution for the highways with ID values 3 and 51 (I-205 NB and I-205 NB Washington) for Wednesdays, Thursdays and Fridays only, within a date range of May 05, 2020 and May 15, 2020.

```
curl "http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/?start_date=2020-05-04&end_date=2020-05-15&days_of_
week=3&days_of_week=4&days_of_week=5&format=csv&highway_id=3&highway_id=54&resolution=01"%"3A00"%"3A00" -H 'Host:
new.portal.its.pdx.edu:8080' -H 'Referer: http://new.portal.its.pdx.edu:8080/downloads/ -o highways_data.csv'
```

#### Curl Example \#3 - Travel Time Data

The following sample query on the Travel Time dataset returns CSV formatted data with a 1 hour resolution, for the I-205 Foster NB and SB segments.

```
curl "http://new.portal.its.pdx.edu:8080/traveltime/api/aggregatedsegmentcalcs/?start_date=2020-05-27
&end_date=2020-05-27&format=csv&resolution=01"%"3A00"%"3A00&segment_id=2264&segment_id=2275" -H 'Host:
new.portal.its.pdx.edu:8080' -H 'Referer: http://new.portal.its.pdx.edu:8080/downloads/ -o travel_time_data.csv'
```

#### Curl Example \#4 - Trimet Data

The following query on the TriMet ridership dataset returns the TriMet for the selected quarter; zip is selected here as that is how the file is served through the website - when unzipped, the data is available in .csv format _only_.

```
curl "http://new.portal.its.pdx.edu:8080/transit/downloadquarterlydata?agency=trimet&quarter=2019-q3-summer"
-H 'Host: new.portal.its.pdx.edu:8080' -H 'Referer: http://new.portal.its.pdx.edu:8080/downloads/ -o trimet.zip'
```

</p>
</details>

<details><summary>Sample Python Requests</summary>
<p>
  
#### The following Python examples will work verbatim in Python 3.6 or later. Earlier versions will require some modification.

#### Python Example \#1 - Highways Data, Single Day

The following sample query on the Highways dataset returns CSV formatted data with a 15 minute resolution for the highways with ID values 3 and 54 (I-205 NB, and I-205 NB Washington) for May 11, 2020.  It then saves that data into a csv file using -o.

```
import requests
import csv

headers = {
        'Host': 'new.portal.its.pdx.edu:8080',
        'Referer': 'http://new.portal.its.pdx.edu:8080/downloads/',
}

params = (
        ('start_date', '2020-05-11'),
        ('end_date', '2020-05-11'),
        ('format', 'csv'),
        ('highway_id', ['3', '54']),
        ('resolution', '00:15:00'),
)
try:
    response = requests.get('http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/',
            headers = headers, params = params)
    response.raise_for_status()
except HTTPError as http_err:
    print(f'HTTP Error: {http_err}')
except Exception as err:
    print(f'Error: {err}')
else:
    print('Writing Output.')

with open('highways_data.csv', 'w+') as file:
    file.write(response.text)
```

#### Python Example \#2 - Highways Data, Limited by Days of Week Over a Range of Dates

The following sample query on the Highways dataset returns CSV formatted data with a 15 minute resolution for the highways with ID values 3 and 51 (I-205 NB and I-205 NB Washington) for Wednesdays, Thursdays and Fridays only, within a date range of May 05, 2020 and May 15, 2020.

```
import requests
import csv

headers = {
        'Host': 'new.portal.its.pdx.edu:8080',
        'Referer': 'http://new.portal.its.pdx.edu:8080/downloads/',
}

params = (
        ('start_date', '2020-05-04'),
        ('end_date', '2020-05-15'),
        ('days_of_week',['3', '4', '5']),
        ('format', 'csv'),
        ('highway_id', ['3', '54']),
        ('resolution', '01:00:00'),
)

try:
    response = requests.get('http://new.portal.its.pdx.edu:8080/highways/api/freewaydata/',
        headers=headers, params=params)
    response.raise_for_status()
except HTTPError as http_err:
    print(f'HTTP Error: {http_err}')
except Exception as err:
    print(f'Error: {err}')
else:
    print('Writing Output.')

with open('highways_data.csv', 'w+') as file:
    file.write(response.text)
```

#### Python Example \#3 - Travel Time Data

The following sample query on the Travel Time dataset returns CSV formatted data with a 1 hour resolution, for the I-205 Foster NB and SB segments. 

```
import requests
import csv

headers = {
        'Host': 'new.portal.its.pdx.edu:8080',
        'Referer': 'http://new.portal.its.pdx.edu:8080/downloads/',
}

params = (
        ('start_date', '2020-05-27'),
        ('end_date', '2020-05-27'),
        ('format', 'csv'),
        ('resolution', '01:00:00'),
        ('setgment_id', ['2264', '2275']),
)

try:
    response = requests.get('http://new.portal.its.pdx.edu:8080/traveltime/api/aggregatedsegmentcalcs/',
            headers=headers, params=params)
    response.raise_for_status()
except HTTPError as http_err:
    print(f'HTTP error occurred: {http_err}')
except Exception as err:
    print(f'Other error occurred: {err}')
else:
    print('Writing Output')

with open('travel_time_data.csv', 'w+') as file:
    file.write(response.text)
```

#### Curl Example \#4 - Trimet Data

The following query on the TriMet ridership dataset returns the TriMet for the selected quarter; zip is selected here as that is how the file is served through the website - when unzipped, the data is available in .csv format _only_.

```
import requests

headers = {
        'Referer': 'http://new.portal.its.pdx.edu:8080/downloads/',
}

params = (
        ('agency', 'trimet'),
        ('quarter', '2019-q3-summer'),
)

try:
    response = requests.get('http://new.portal.its.pdx.edu:8080/transit/downloadquarterlydata',
            headers = headers, params=params)
    response.raise_for_status()
except HttpError as http_err:
    print(f'HTTP Error: {http_err}')
except Exception as err:
    print(f'Error: {err}')
else:
    print('Downloading Zip File.')
with open('transit_data.zip', 'wb') as zipfile:
    for chunk in response.iter_content(128):
        zipfile.write(chunk)
```

</p>
</details>
Last Updated: 2020-07-07
