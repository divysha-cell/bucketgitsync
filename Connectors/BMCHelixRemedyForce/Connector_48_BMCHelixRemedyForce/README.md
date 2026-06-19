# Connector_48_BMCHelixRemedyForce
Pull information about incidents from BMC Helix Remedyforce.


Integration: BMCHelixRemedyForce

Integration Version: 18

Device Product Field: Product Name

Event Name Field: BMCServiceDesk__Type__c
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the BMC Helix Remedyforce instance.|True|https://127.0.0.1|
|Login API Root|API root that is used to authenticate in BMC Helix Remedyforce.|True|https://login.salesforce.com|
|Username|BMC Helix Remedyforce username.|False|dummy_valid_string|
|Password|BMC Helix Remedyforce password.|False|*****|
|Client ID|BMC Helix Remedyforce client ID of the connected app. This parameter is needed for OAuth authentication. Note: this parameter has priority over Username + Password authentication.|False|3|
|Client Secret|BMC Helix Remedyforce client secret of the connected app. This parameter is needed for OAuth authentication. Note: this parameter has priority over Username + Password authentication.|False|*****|
|Refresh Token|Refresh token for the OAuth authorization.|False|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the BMC Helix Remedyforce server is valid.|False|true|
|Lowest Priority To Fetch|Lowest priority that will be used to fetch incidents. Maximum: 5. Minimum: 1. If nothing is provided, the connector will ingest all incidents.|False|3|
|Ingest Empty Priority Incidents|If enabled, the connector will fetch incidents that don't have priority. Siemplify Alerts created in this manner will have priority set to "Informational".|False|3|
|Type Filter|Type filter for the incidents. If nothing is provided, the connector will ingest all incidents. Example: Incident, Service Request.|False|Incident,Service Request|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Maximum is 200.|False|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

