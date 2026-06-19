# Connector_30_CiscoAMP
Pull security events from Cisco AMP into Siemplify. Note: whitelist works with eventType parameter.


Integration: CiscoAMP

Integration Version: 24

Device Product Field: Product Name

Event Name Field: event_type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic.|False|.*|
|API Root|API root of the Cisco AMP instance.|False|https://127.0.0.1|
|Client ID|Client AMP Client ID.|True|dummy_valid_string|
|API Key|Cisco AMP API Key.|True|*****|
|Lowest Severity To Fetch|Severity that will be used to fetch events. If nothing is specified, connector will ingest all events. Possible values: Low, Medium, High, Critical.|False|dummy_valid_string|
|Fetch Events Without Severity|If enabled, the connector will fetch events that don't have severity. Those events will be assigned "Informational" severity.|False|true|
|Max Events To Fetch|How many alerts to process per one connector iteration. Maximum is 1000. Default: 100.|True|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Proxy Server Address|Proxy server address.|False|https://127.0.0.1|
|Proxy Username|Proxy username.|False|dummy_valid_string|
|Proxy Password|Proxy password.|False|*****|
|Verify SSL|If enabled,, verify the SSL certificate for the connection to the Cisco AMP server is valid.|False|true|

