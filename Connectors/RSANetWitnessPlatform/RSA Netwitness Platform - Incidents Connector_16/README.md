# RSA Netwitness Platform - Incidents Connector_16
Pull incidents from RSA Netwitness Platform.


Integration: RSANetWitnessPlatform

Integration Version: 18.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Web API Root|Web API Root of the RSA Netwitness Platform instance.|True|https://{ip}/rest/api|
|Web Username|Username of the RSA Netwitness Platform account.|True|0|
|Web Password|Password of the RSA Netwitness Platform account.|True|*****|
|Broker API Root|API Root of the RSA Netwitness broker. Note: broker configuration takes priority over concentrator. Example: https://{ip}:50103. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|0|
|Broker API Username|API Username of the RSA Netwitness broker. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|0|
|Broker API Password|API Password of the RSA Netwitness broker. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|*****|
|Concentrator API Root|API Root of the RSA Netwitness concentrator. Note: broker configuration takes priority over concentrator. Example: https://{ip}:50105. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|0|
|Concentrator API Username|API Username of the RSA Netwitness concentrator. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|0|
|Concentrator API Password|API Password of the RSA Netwitness concentrator. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|*****|
|Credential JSON Object|This parameter is needed for storing the data source credentials. This parameter has priority over "Broker API Root", "Broker API Username", "Broker API Password", "Concentrator API Root", "Concentrator API Username", "Concentrator API Password". Please refer to the documentation portal for more details.|False|*****|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Note: connector will wait for the provided time for the updates to incidents.|False|1|
|Lowest Risk Score To Fetch|Lowest risk score of the incidents to fetch. By default, the connector will ingest all of the incidents. Maximum is 100.|False|0|
|Severity Fallback|Specify what should be the fallback severity for the Siemplify Alert, when risk score is not available. Possible values: Informational, Low, Medium, High, Critical.|True|Informational|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Maximum is 100.|False|10|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the RSA Netwitness Plaform server is valid.|False|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|

