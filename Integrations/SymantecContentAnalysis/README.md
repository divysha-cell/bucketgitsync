
# SymantecContentAnalysis

Symantec Content Analysis automatically escalates and brokers zero-day threats for dynamic sandboxing and validation before sending content to users. Analyze unknown content from one central location.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|URL|https://x.x.x.x:8082/|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|charset_normalizer-3.4.6-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|


## Actions
#### Get Hash Report
Get samples for hash (MD5 and SHA256)
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Submit File
Upload file to Symantec Content Analysis for a scan
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|Submit file from path.|True|String|None|









