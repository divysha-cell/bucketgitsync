# Connector_42_AzureSecurityCenter
Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Pull security alerts from Azure Security Center. Note: whitelist works with alertType field.


Integration: AzureSecurityCenter

Integration Version: 17

Device Product Field: Product Name

Event Name Field: properties_entities_type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Client ID|Client ID of the Microsoft Azure application. |True|dummy_valid_string|
|Client Secret|Client Secret of the Microsoft Azure application.|True|*****|
|Username|Username of the Microsoft Azure account.|False|dummy_valid_string|
|Password|Password of the Microsoft Azure account.|False|*****|
|Subscription ID|Subscription ID of the Microsoft Azure application.|True|dummy_valid_string|
|Tenant ID|Tenant ID of the Microsoft Azure application.|True|dummy_valid_string|
|Refresh Token|Refresh token for the OAuth authorization.|False|*****|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|50|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch Alert. Possible values: Low, Medium, High|True|Low|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Azure Security Center server is valid.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

