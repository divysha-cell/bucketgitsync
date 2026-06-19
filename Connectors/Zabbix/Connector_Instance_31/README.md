# Connector_Instance_31
Automated connector 31


Integration: Zabbix

Integration Version: 17

Device Product Field: Product Field Name

Event Name Field: Event Field Name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Api Root|Api Root|True|dummy_val|
|Username|Username|True|dummy_val|
|Password|Password|True|*****|
|Only Problematic Triggers|If enabled, only problematic triggers will be considered.|False|False|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|24|
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Zabbix server is valid.|False|false|

