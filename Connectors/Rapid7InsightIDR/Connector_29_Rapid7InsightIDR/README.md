# Connector_29_Rapid7InsightIDR
This connector was built using API endpoints that are in preview release. Pull information about investigation from Rapid7 InsightIDR. Note: Dynamic list filter works with the "title" parameter.


Integration: Rapid7InsightIDR

Integration Version: 13

Device Product Field: data_type

Event Name Field: source
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Rapid7 InsightIDR instance.|True|https://127.0.0.1|
|API Key|API Key of the Rapid7 InsightIDR account.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Rapid7 InsightIDR server is valid.|False|true|
|Sources|Sources that will be used to fetch investigations. Possible values: User, Alert. If nothing is provided, the connector will ingest investigations from both sources.|False|ALERT,USER|
|Lowest Priority To Fetch|The lowest priority that needs to be used to fetch investigations. Possible values: Low, Medium, High, Critical. If nothing is specified, the connector ingests alerts with all severities.|False|4|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve investigations from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|Number of alerts to process per one connector iteration. Default: 20.|False|20|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

