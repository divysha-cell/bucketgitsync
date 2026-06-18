# Zabbix Connector_1
Zabbix connector - fetches events from Zabbix.


Integration: Zabbix

Integration Version: 17.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|300|
|Api Root|Api Root|True|0|
|Username|Username|True|0|
|Password|Password|True|*****|
|Only Problematic Triggers|If enabled, only problematic triggers will be considered.|False|False|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|24|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Zabbix server is valid.|False|false|

