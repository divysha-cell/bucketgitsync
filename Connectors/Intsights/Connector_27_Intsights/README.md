# Connector_27_Intsights
Configured Connector_27_Intsights


Integration: Intsights

Integration Version: 28

Device Product Field: Details_Source_NetworkType

Event Name Field: Details_Title
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Api Root|The api root of the Intsights server|True|https://api.intsights.com|
|Account ID|The account ID to login with|True|dummy_valid_string|
|Api Key|The API key to login with.|True|*****|
|Verify SSL|Whether to verify the SSL certificate of the server|False|FALSE|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|3|
|Max Alerts Per Cycle|Max number of alerts to fetch per single connector cycle|True|10|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

