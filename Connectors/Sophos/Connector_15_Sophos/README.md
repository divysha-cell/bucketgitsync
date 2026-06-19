# Connector_15_Sophos
Pull alerts from Sophos Central into Siemplify. Note: alerts are available to API only for 24 hours.


Integration: Sophos

Integration Version: 22

Device Product Field: Product Name

Event Name Field: type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Sophos instance.|True|https://127.0.0.1|
|API Key|Sophos API key.|False|*****|
|Base 64 Auth Payload|Sophos Base 64 Auth Payload. Note: "Basic" shouldn't be a part of it.|False|*****|
|Client ID|Sophos Client ID.|False|dummy_valid_string|
|Client Secret|Sophos Client Secret.|False|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Sophos Central server is valid.|False|true|
|Lowest Severity To Fetch|Severity that will be used to fetch alerts. If nothing is specified, action will ingest all alerts. Possible values: Low, Medium, High.|False|dummy_valid_string|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Maximum is 24 hours.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Maximum is 1000.|False|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

