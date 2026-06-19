# Connector_52_DigitalShadows
Connector ingest incidents from Digital Shadows into Siemplify.


Integration: DigitalShadows

Integration Version: 13

Device Product Field: Product Name

Event Name Field: type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Max Incidents To Fetch|How many incidents to process per one connector iteration.|False|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Digital Shadow server is valid.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Key|Digital Shadow API Key.|True|dummy_valid_string|
|API Secret|Digital Shadow API Secret.|True|*****|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch findings. Possible values: VERY_HIGH, HIGH, MEDIUM, LOW, VERY_LOW, NONE|True|NONE|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Incident Type Filter|Comma-separated list of incident types that should be ingested into Siemplify. By default connector pulls all of the incident types. Example: DATA_LEAKAGE,CYBER_THREAT. Possible Values: DATA_LEAKAGE, CYBER_THREAT, PHYSICAL_SECURITY, SOCIAL_MEDIA_COMPLIANCE, BRAND_PROTECTION, INFRASTRUCTURE.|False|dummy_valid_string|

