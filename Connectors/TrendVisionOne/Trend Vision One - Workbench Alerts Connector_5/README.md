# Trend Vision One - Workbench Alerts Connector_5
Pull information about workbench alerts from Trend Vision One. Note: dynamic list filter works with "model" parameter.


Integration: TrendVisionOne

Integration Version: 10.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field through regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|API Root|API root of the Trend Vision One instance.|True|https://{instance}|
|API Token|API Key of the Trend Vision One account.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Trend Vision One server is valid.|False|true|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch alerts. Possible values: Low, Medium, High, Critical. If nothing is specified, the connector will ingest alerts with all severities.|False|0|
|Max Hours Backwards|Amount of hours from where to fetch alerts.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Default: 10.|False|10|
|Use dynamic list as a blocklist|If enabled, dynamic lists will be used as a blocklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|

