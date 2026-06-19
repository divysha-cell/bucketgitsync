
# Wildfire

Cloud-based threat analysis and prevention engine for highly evasive zero-day exploits and malware.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key||True|Password|*****|


#### Dependencies
| |
|-|
|xmltodict-0.13.0-py2.py3-none-any.whl|
|pan_python-0.25.0-py3-none-any.whl|


## Actions
#### GetReport
Get a detonation report from WildFire
Timeout - 600 Seconds



#### GetPcap
Download and save the PCAP file of a sample from WildFire
Timeout - 600 Seconds



#### GetFile
Download and save a sample from WildFire
Timeout - 600 Seconds



#### DetonateFile
Upload file to WildFire and retrieve report
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|File Paths|True|String|Detonate file from path(e.g: C:\temp\NPPJSONViewer.dll).|



#### Ping
Test connectivity to Wildfire
Timeout - 600 Seconds









