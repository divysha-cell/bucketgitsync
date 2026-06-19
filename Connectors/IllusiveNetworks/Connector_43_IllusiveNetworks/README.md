# Connector_43_IllusiveNetworks
Pull incidents with related forensic timeline from Illusive Networks. Note: This connector requires changes to the rate limiting on the Illusive Networks server. Default rate limit is too small. All of the steps are available in the documentation. Whitelisting and Blacklisting is done via type of the incident


Integration: IllusiveNetworks

Integration Version: 9

Device Product Field: Product Name

Event Name Field: details_serviceType
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Illusive Networks instance.|True|https://127.0.0.1|
|API Key|API Key of the Illusive Networks. Note: string "Basic" shouldn't be a part of the value.|True|*****|
|CA Certificate File|Base 64 encoded CA certificate file.|False|dummy_valid_string|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Illusive Networks server is valid.|False|false|
|Alert Severity|Severity of the Siemplify alert that will be created based on the incidents from Illusive Networks. Possible values: Informational Low Medium High Critical|True|Medium|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Maximum is 1000.|False|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

