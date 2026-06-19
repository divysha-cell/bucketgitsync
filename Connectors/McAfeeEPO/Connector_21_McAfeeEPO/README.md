# Connector_21_McAfeeEPO
Pull events from the EPOEvents table into Siemplify. Whitelist works with Analyzer names.


Integration: McAfeeEPO

Integration Version: 38

Device Product Field: Product Name

Event Name Field: EPOEvents_ThreatType
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the McAfee ePO instance.|True|https://127.0.0.1|
|Username|Username of the McAfee ePO instance.|True|dummy_valid_string|
|Password|Password of the McAfee ePO instance.|True|*****|
|Group Name|If provided, the connector will only fetch threats from endpoints that are a part of that group.|False|dummy_valid_string|
|CA Certificate File|Base 64 encoded CA certificate file.|False|dummy_valid_string|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the McAfee ePO server is valid.|False|false|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Lowest Severity To Fetch|Lowest severity of the events to fetch. By default, the connector will ingest all of the events. Possible Values: Info, Low, Medium, High, Critical.|False|Medium|
|Max Events To Fetch|How many events to process per one connector iteration. Default: 10.|False|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

