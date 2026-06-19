# Connector_36_LogRhythm
Pull alerts from LogRhythm using Rest API. Note: this connector is only supported for LogRhythm version 7.7+.


Integration: LogRhythm

Integration Version: 23

Device Product Field: Product Name

Event Name Field: classificationTypeName
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|API Root|API root of the LogRhythm instance.|True|https://127.0.0.1|
|API Token|LogRhythm API token.|True|*****|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alarms To Fetch|How many alerts to process per one connector iteration.|False|10|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the LogRhythm server is valid.|False|false|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

