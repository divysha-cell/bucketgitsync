# Connector_14_StellarCyberStarlight
Pull security events from Stellar Cyber Starlight.  Note: dynamic list works with the Chronicle SOAR alert name, which can be either “event_category: event_name” or “_source_xdr_event_xdr_killchain_stage:_source_xdr_event_name”


Integration: StellarCyberStarlight

Integration Version: 19

Device Product Field: Product Name

Event Name Field: _source_event_name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API Root of the Stellar Cyber Starlight instance.|True|https://127.0.0.1|
|Username|Username of the Stellar Cyber Starlight account.|True|dummy_valid_string|
|API Key|API Key of the Stellar Cyber Starlight account. This parameter was used for Basic Authentication. If both “API Key” and “API Token” is provided, “API Token” will have priority.|False|*****|
|API Token|API Token of the Stellar Cyber Starlight account. This parameter was used for JWT Authentication. If both “API Key” and “API Token” is provided, “API Token” will have priority.|False|*****|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch events.|True|50|
|Padding Period|Padding period (hours) for the connector execution.|False|0|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Events To Fetch|How many events to process per one connector iteration.|False|50|
|Timestamp Field|Field that will be used for managing time in the connector. Supported values: timestamp, write_time|True|timestamp|
|Product Field Fallback|Specify a comma separated list of incident or alert attributes that should be used as a fallback for the "Product Field Name" parameter and "DeviceProduct" field in descending order. First attribute will have the highest priority, next if its not present or empty in the event - fallback to the next value from the list and so on.|False|4|
|Event Field Fallback|Specify a comma separated list of alert attributes that should be used as a fallback for the "Event Field Name" parameter in descending order. First attribute will have the highest priority, next if it's not present or empty in the event - fallback to the next value from the list and so on. Note: this parameter will introduce a new key in the event data called "chronicle_event_type". Use this key in the "Event Field Name" parameter to be able to utilize the fallback logic.|False|4|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Stellar Cyber Starlight server is valid.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

