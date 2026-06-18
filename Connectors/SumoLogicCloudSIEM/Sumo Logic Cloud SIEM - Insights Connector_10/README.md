# Sumo Logic Cloud SIEM - Insights Connector_10
Pull information about insights from Sumo Logic Cloud SIEM. Note: dynamic list filter works with "name" parameter.


Integration: SumoLogicCloudSIEM

Integration Version: 14.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|API Root|API root of the Sumo Logic Cloud SIEM instance.|True|https://{instance}|
|API Key|API Key of the Sumo Logic Cloud SIEM account. Note: API key has priority over other authentication method.|False|*****|
|Access ID|Access ID of the Sumo Logic Cloud SIEM account. Note: both Access ID and Access Key are required for this type of authentication.|False|0|
|Access Key|Access Key of the Sumo Logic Cloud SIEM account. Note: both Access ID and Access Key are required for this type of authentication.|False|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Sumo Logic Cloud SIEM server is valid.|False|true|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch insights. Possible values: Low, Medium, High, Critical. If nothing is specified, the connector will ingest insights with all severities.|False|0|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve insights from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Insights To Fetch|How many insights to process per one connector iteration. Default: 20.|False|20|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|

