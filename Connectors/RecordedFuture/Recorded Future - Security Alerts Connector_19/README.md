# Recorded Future - Security Alerts Connector_19
Pull security alerts from Recorded Future. 
Whitelist and blacklist work with Recorded Future rule names.


Integration: RecordedFuture

Integration Version: 23.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|API URL|API Root of the Recorded Future instance.|True|https://api.recordedfuture.com|
|API Key|API Key of the Recorded Future.|True|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|100|
|Severity|Severity will be one from the following values Low, Medium, High, Critical. Will be assigned to Siemplify alerts created from this connector.|True|Medium|
|Get Alert's Details|Get alert's full details from Recorded Future. Note: each query "costs" 1 Recorded Future API credit.|False|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Recorded Future server is valid.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|

