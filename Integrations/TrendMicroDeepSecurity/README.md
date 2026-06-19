
# TrendMicroDeepSecurity

Hybrid cloud security that matches the performance and flexibility of today's virtualised data centre

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://<host or IP>:<port>|
|Api Secret Key||True|Password|*****|
|Api Version||True|String|v1|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|TIPCommon-1.0.15-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Scan Host
Request a malware scan
Timeout - 600 Seconds



#### Get Security Profiles
Get all of the policies from Deep Security
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Get Host Info
Describe a computer
Timeout - 600 Seconds



#### Assign Security Profile To Host
Assign the specified policy to computers
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Profile Name|Policy name.|True|String|None|









