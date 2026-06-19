# Connector_17_Splunk
Splunk Pull Connector


Integration: Splunk

Integration Version: 65

Device Product Field: Product Name

Event Name Field: app
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Alerts Count Limit|Limit the number of Alerts returned by the connector per 1 iteration.|False|100|
|Server Address|IP Address of Splunk API Server.|True|https://127.0.0.1|
|Port|Port of the Splunk Instance.|True|8089|
|Username|Splunk account username.|False|dummy_valid_string|
|Password|Splunk account password.|False|*****|
|API Token|Splunk API Token. API token has priority over other authentication methods, when this field is not empty.|False|*****|
|Time Frame|Time frame of alerts to fetch. Examples: 1m - from 1 minute ago 3h - from 3 hours ago 1d - from 24 hours ago (1 day) 1w - from 1 week ago.|False|1h|
|Verify SSL|Whether to verify ssl certificate on connection or not.|False|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is "".|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return value unchanged. Used to allow the user to manipulate the environment field via regex logic. If regex pattern is null or empty, or the environment value is null, the final environment result is "".|False|.*|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|CA Certificate File|CA Certificate File|False|dummy_valid_string|

