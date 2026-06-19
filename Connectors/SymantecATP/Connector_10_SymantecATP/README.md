# Connector_10_SymantecATP
Fetch incidents from Symantec ATP


Integration: SymantecATP

Integration Version: 13

Device Product Field: Product Name

Event Name Field: AlertName
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.
Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of Symantec ATP server.|True|https://127.0.0.1|
|Client ID|Symantec ATP Client ID|True|*****|
|Client Secret|Symantec ATP Client Secret|True|*****|
|Priority Filter|Priority filter for the incidents. If you want to ingest all of the incidents specify: Low, Medium, High.|True|5|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Limit: 30 days. This is a Symantec ATP limitation.|False|1|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Max: 1000.|False|25|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Use SSL|Option to enable SSL/TLS connection|False|true|
|Proxy Server Address|The address of the proxy server to use|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with|False|*****|

