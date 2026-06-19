
# StealthwatchV6-10

Cisco Stealthwatch provides pervasive network visibility and sophisticated security analytics for advanced protection across the extended network and cloud.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|IP_OR_HOST|https://x.x.x.x|
|Username||True|String||
|Password||True|Password|*****|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|charset_normalizer-3.4.6-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|


## Actions
#### Search Events
Get a host's security events for a given time frame
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Timeframe|Time frame in hours.|True|String||



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Search Flows
Get flows by IP address for a given time frame
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Timeframe|Time frame in hours(e.g: 3).|True|String||
|Limit|The limit of the recieved flow.|True|String||









