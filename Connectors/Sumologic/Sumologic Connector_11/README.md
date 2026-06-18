# Sumologic Connector_11
Sumologic Connector


Integration: Sumologic

Integration Version: 20.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|180|
|Api Root|The Sumologic Api root, i.e: https://api.{region}.sumologic.com|True|0|
|Access ID|Sumologic access ID|False|0|
|Access Key|Sumologic access key|False|*****|
|Verify SSL|Whether to use ssl on connection or not|False|false|
|Alert Name Field|The name of the field where the alert name is located (flat field path). e.g. _sourcecategory|True|_sourcecategory|
|Timestamp Field|The name of the field where the timestamp is located (flat field path). e.g. _receipttime|True|_receipttime|
|Environment Field|The name of the field where the environment is located (flat field path). e.g. _collector|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Indexes|Indexes to get alerts in|False|*|
|Alerts Count Limit|Max count of alerts to pull in one cycle. e.g. 20|True|10|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alerts since. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. e.g. 3|True|1|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|

