
# Stealthwatch

Cisco Stealthwatch provides pervasive network visibility and sophisticated security analytics for advanced protection across the extended network and cloud.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|IP_OR_HOST|https://x.x.x.x|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|false|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Search Flows
Get flows by IP address for a given time frame
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Timeframe|Time frame in hours(e.g: 3).|True|String||
|Limit|The limit of the recieved flow.|True|String||



#### Search Events
Get a host's security events for a given time frame
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Timeframe|Time frame in hours.|True|String||



#### Ping
Test Connectivity
Timeout - 600 Seconds









