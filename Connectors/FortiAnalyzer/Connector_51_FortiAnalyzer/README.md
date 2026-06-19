# Connector_51_FortiAnalyzer
Pull information about alerts from FortiAnalyzer. Note: Dynamic list filter works with the "subject" parameter.


Integration: FortiAnalyzer

Integration Version: 12

Device Product Field: siemplify_type

Event Name Field: eventtype
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field through regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the FortiAnalyzer instance.|True|https://127.0.0.1|
|Username|Username of the FortiAnalyzer account.|True|dummy_valid_string|
|Password|Password of the FortiAnalyzer account.|True|*****|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the FortiAnalyzer server is valid.|False|true|
|Lowest Severity To Fetch|The lowest severity that needs to be used to fetch alerts. Possible values: low, medium, high, critical. If nothing is specified, the connector ingests alerts with all severities.|False|Medium|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|Number of alerts to process per one connector iteration. Default: 20.|False|20|
|Use dynamic list as a blacklist|If enabled, the dynamic list is used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

