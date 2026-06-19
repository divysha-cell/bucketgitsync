# Connector_34_FireEyeNX
Connector ingests FireEye NX alert into Siemplify.


Integration: FireEyeNX

Integration Version: 12

Device Product Field: Product Name

Event Name Field: name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of FireEye NX server.|True|https://127.0.0.1|
|Username|Username of the FireEye NX account.|True|dummy_valid_string|
|Password|Password of the FireEye NX account.|True|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye NX server is valid.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

