# Connector_47_Phishrod
Pull information about incidents from PhishRod. Note: dynamic list filter works with “emailSubject” parameter.


Integration: Phishrod

Integration Version: 5

Device Product Field: Product Name

Event Name Field: Event Field
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored.
If the environment field isn't found, the environment is the default environment.
|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged.
Used to allow the user to manipulate the environment field via regex logic.
If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.
|False|.*|
|API Root|API root of the Phishrod instance.|True|https://127.0.0.1|
|API Key|API key of the Phishrod account. |True|*****|
|Client ID|Client ID of the Phishrod account.|True|*****|
|Username|Username of the Phishrod account.|True|dummy_valid_string|
|Password|Password of the Phishrod account.|True|*****|
|Alert Severity|Set the severity for the alert based on the incident. Possible values: Informational, Low, Medium, High, Critical.|True|Medium|
|Use dynamic list as a blacklist|If enabled, the dynamic list is used as a blacklist.|False|false|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the PhishRod server is valid.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

