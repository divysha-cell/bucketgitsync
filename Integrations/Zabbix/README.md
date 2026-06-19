
# Zabbix

Zabbix is an enterprise open source monitoring software for networks and applications.
It is designed to monitor and track the status of various network services, servers, and other network hardware.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|IP_OR_HOST|http://{IP}/zabbix|
|Username||True|String|None|
|Password||True|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|idna-3.8-py3-none-any.whl|
|TIPCommon-1.0.16-py2.py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|pyzabbix-1.3.1-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|packaging-24.1-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|certifi-2024.8.30-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|


## Actions
#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Execute Script
Execute a script on hosts by IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Script Name|The name of the script to execute.|True|String||



##### JSON Results
```json
[{"EntityResult": {"response": "success", "value": "sudo: no tty present and no askpass program specified\n"}, "Entity": "1.1.1.1"}]
```









## Connectors
#### Zabbix Connector
Zabbix connector - fetches events from Zabbix.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|Api Root|True|String||
|Username|Username|True|String||
|Password|Password|True|Password|*****|
|Only Problematic Triggers|If enabled, only problematic triggers will be considered.|False|Boolean|False|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Zabbix server is valid.|False|Boolean|false|


##### Allowlist
| |
|-|
|tag_name_value|




