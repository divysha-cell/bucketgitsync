# ServiceNow Connector_17
Fetching incidents from ServiceNow to Siemplify


Integration: ServiceNow

Integration Version: 67.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Username|Username|True|0|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|60|
|Rule Generator|The field name used to determine the rule generator.|False|0|
|Api Root|https://{dev-instance}.service-now.com/api/now/v1/|True|0|
|Incident Table|This parameter is defining what API root ServiceNow integration is going to use for actions that revolve around incidents. By default the integration uses the “table/incident” path. |False|incident|
|Password|Password|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the ServiceNow server is valid.|False|true|
|Client ID|Client ID of Service Now application. Required for Oauth authentication.|False|0|
|Client Secret|Client Secret of Service Now application. Required for Oauth authentication.|False|*****|
|Refresh Token|Refresh token for Service Now application. Required for Oauth authentication.|False|*****|
|Assignment Group|Name of the assignment group for which you want to ingest records.|False|0|
|Use sys_domain Environment|When enabled, the connector will use the incident's 'sys_domain' from ServiceNow as the environment for the ingested case. If the field doesn't exist, connector will use the environment defined in the 'Environment' parameter.|False|true|
|Use Oauth Authentication|If enabled, integration will use Oauth authentication. Parameters “Client ID“, “Client Secret“ and “Refresh Token“ are mandatory.|False|false|
|Days Backwards|Fetch incidents from 'x' days backwards. e.g. 3|False|5|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|false|
|Max Incidents Per Cycle|Fetch max 'x' incidents. e.g. 10|False|10|
|Server Time Zone|The timezone configured in the server, ex. UTC, Asia/Jerusalem etc.|False|UTC|
|Environments Whitelist|The environments (domains) to ingest into Siemplify, comma separated list (env1,env2)|False|0|
|Table Name|The table to fetch from. e.g. incident|False|0|
|Event Name|The name of the event in Siemplify. e.g. ServiceNowEvent|False|0|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Get User Information|If enabled, connector will additionally retrieve information about the users related to the incident.|False|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|

