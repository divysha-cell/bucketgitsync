# Connector_49_NozomiNetworks
Connector to fetch Nozomi Networks Alerts to Siemplify.


Integration: NozomiNetworks

Integration Version: 11

Device Product Field: Product Name

Event Name Field: Operation
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API URL|Nozomi API URL to connect to.|True|https://127.0.0.1|
|Username|Nozomi account username to use for connection.|True|dummy_valid_string|
|Password|Nozomi account password to use for connection.|True|*****|
|Verify SSL|Specify whether API URL certificate should be validated before connection.|False|false|
|CA Certificate File|CA Certificate File - parsed into Base64 String.|False|dummy_valid_string|
|Minimum severity to fetch|Minimum severity alert should have to be ingested, severity can be a number from 0 to 10.|False|10|
|Ingest only alerts that have “is_security” attribute set to True?|Specify if only alerts that have “is_security” attribute set to True should be ingested.|False|false|
|Ingest only alerts that have “is_incident” attribute set to True?|Specify if only alerts that have “is_incident” attribute set to True should be ingested.|False|false|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|8|
|Fetch Backwards Time Interval (minutes)|Time interval connector should use to fetch alerts from max hours backwards. If Nozomi Device is deployed in a large network, the number of generated alerts can be substantial. Because of this, this parameter in minutes can be used to split max hours backwards on smaller segments and process them individually. Time interval cant be bigger than max hours backwards value.|True|60|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

