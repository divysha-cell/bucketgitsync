# Connector_2_Zabbix
Zabbix connector - fetches events from Zabbix.


Integration: Zabbix

Integration Version: 17

Device Product Field: Product Field Name

Event Name Field: Event Field Name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Api Root|Api Root|True|https://127.0.0.1|
|Username|Username|True|dummy_valid_string|
|Password|Password|True|*****|
|Only Problematic Triggers|If enabled, only problematic triggers will be considered.|False|False|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|24|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Zabbix server is valid.|False|false|

