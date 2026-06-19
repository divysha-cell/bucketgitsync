# Connector_25_GoogleThreatIntelligence
Use the Google Threat Intelligence - DTM Alerts Connector to retrieve alerts from Google Threat Intelligence. The dynamic listworks with the "alert_type" parameter.


Integration: GoogleThreatIntelligence

Integration Version: 15

Device Product Field: Product Name

Event Name Field: event_type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment. The default value is "".|False|dummy_valid_string|
|Environment Regex Pattern|A regular expression pattern to run on the value found in the "Environment Field Name" field. This parameter lets you manipulate the environment field using the regular expression logic.Use the default value ".*" to retrieve the|False|.*|
|API Root|The API root of the Google Threat Intelligence instance.|True|https://www.virustotal.com|
|API Key|The Google Threat Intelligence API key.|True|*****|
|Verify SSL|If selected, the connector verifies that the SSL certificate for connecting to Google Threat Intelligence is valid.|False|true|
|Lowest Severity To Fetch|The lowest severity of the alerts to fetch. If you don’t set a value, the connector ingests alerts with all severity levels. The possible values are as follows: Low, Medium, High.|False|dummy_valid_string|
|Monitor ID Filter|A comma-separated list of monitor IDs from which to retrieve alerts. This parameter is applied alongside side Monitor Name values as OR filter.|False|dummy_valid_string|
|Monitor Name Filter|A comma-separated list of monitor names from which to retrieve alerts. Note: if there are several monitors with the same name, connector will ingest from all of them. This parameter is applied alongside side Monitor ID values as OR filter.|False|dummy_valid_string|
|Event Type Filter|A comma-separated list of event types that needs to be returned. If input is provided in format “!event_type”, then action will return all events except for the provided one. If nothing is provided, the connector will process all event types. Input is case sensitive.|False|dummy_valid_string|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation. Selected by default.|False|true|
|Max Hours Backwards|The number of hours before the first connector iteration to retrieve responses from. This parameter applies either to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp. The default value is 1 hour.|True|1|
|Max Alerts To Fetch|The maximum number of alerts to process for every connector iteration. The default value is 25. The maximum value is 25.|True|25|
|Use dynamic list as a blocklist|If selected, the connector uses th dynamic list as a blocklist. Not selected by default.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

