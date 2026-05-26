# cdemnAlienVault USM Appliance Connector
asdfghjgfdsadfghjhgfdsdfghj


Integration: AlienVaultAppliance

Integration Version: 26.0

Device Product Field: device_product

Event Name Field: name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|60|
|Api Root|e.g. https://<instance>.alienvault.com|True|sf|
|Username|Username|True|v|
|Password|Password|True|*****|
|Max Events Per Alert|Limit the number of events per alert. e.g. 10|True|10|
|Max Days Backwards|This field is used in the connector first running cycle and determine the connector start time. e.g. 3|True|1|
|Max Alerts Per Cycle|Limit the number of alerts in every cycle. e.g. 10|True|10|
|Server Timezone|The timezone configured in the AlienVault's, ex. UTC, Asia/Jerusalem etc.|True|UTC|
|Environment Field Name|The name of the environment's field. e.g. AlienVault Sensor|False||
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False|*****|


Addon !@12