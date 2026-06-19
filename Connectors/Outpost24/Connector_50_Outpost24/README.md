# Connector_50_Outpost24
Pull information about outscan findings from Outpost24. Note: whitelist filter works with "productName" parameter.


Integration: Outpost24

Integration Version: 10

Device Product Field: Product Name

Event Name Field: type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Outpost24 instance.|True|https://your-appliance.outpost24.com|
|Username|Username of the Outpost24 account.|True|dummy_valid_string|
|Password|Password of the Outpost24 account.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Outpost24 server is valid.|False|true|
|Lowest Risk To Fetch|Lowest risk that needs to be used to fetch alerts. Possible values: Initial, Recommendation, Low, Medium, High, Critical. If nothing is specified, the connector will ingest alerts with all risk levels.|False|dummy_valid_string|
|Type Filter|Comma-separated list of type filters for the finding. Possible values: Vulnerability, Information, Port.|True|Vulnerability, Information, Port|
|Max Days Backwards|Number of hours before the first connector iteration to retrieve findings from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Findings To Fetch|How many findings to process per one connector iteration. Default: 100.|False|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

