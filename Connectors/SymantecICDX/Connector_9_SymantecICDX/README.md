# Connector_9_SymantecICDX
Fetching events from SymantecICDX server using a query


Integration: SymantecICDX

Integration Version: 10

Device Product Field: device_product

Event Name Field: name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Api Root|Api Root|True|https://127.0.0.1|
|Api Token|Api Token|True|*****|
|Verify SSL|Whether to use ssl on connection or not|False|FALSE|
|Search Query|Search Query|True|dummy_valid_string|
|Events Limit|Max count of events to pull in one cycle. e.g. 20|True|10|
|Max Days Backwards|Max number of days to fetch events since. e.g. 3|True|1|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

