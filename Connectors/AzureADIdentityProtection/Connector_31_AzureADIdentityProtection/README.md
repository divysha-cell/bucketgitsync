# Connector_31_AzureADIdentityProtection
Pull information about risk detections from Azure AD Identity Protection. Note: whitelist filter works with "riskEventType" parameter.


Integration: AzureADIdentityProtection

Integration Version: 9

Device Product Field: Product Name

Event Name Field: riskEventType
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Azure AD Identity Protection instance.|True|https://graph.microsoft.com|
|Login API Root|Login API root of the Azure AD Identity Protection instance.|False|https://login.microsoftonline.com|
|Tenant ID|Tenant ID of the Azure AD Identity Protection account.|True|dummy_valid_string|
|Client ID|Client ID of the Azure AD Identity Protection account.|True|dummy_valid_string|
|Client Secret|Client Secret of the Azure AD Identity Protection account.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Azure AD Identity Protection server is valid.|False|true|
|Lowest Risk Level To Fetch|Lowest risk that needs to be used to fetch alerts. Possible values: Low, Medium, High. If nothing is specified, the connector will ingest risk detections with all risk levels.|False|dummy_valid_string|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve risk detections from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Default: 100.|False|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

