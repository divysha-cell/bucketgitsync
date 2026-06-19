# Connector_40_GoogleAlertCenter
Pull information about alerts from Google Alert Center. Note: whitelist filter works with "type" parameter.


Integration: GoogleAlertCenter

Integration Version: 11

Device Product Field: source

Event Name Field: type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Service Account JSON Secret|JSON that contains the secret of service account keys.|True|*****|
|Impersonation Email Address|Email address that has access to the alert center.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Alert Center server is valid.|False|true|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Default: 100.|False|100|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch alerts. Possible values: Informational, Low, Medium, High. If nothing is specified, the connector will ingest alerts with all severities.|False|dummy_valid_string|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

