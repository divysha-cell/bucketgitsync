# Connector_44_Devo
Connector can be used to fetch alert records from Devo siem.logtrust.alert.info table. Connector whitelist can be used to ingest only specific types of alerts based on alert context value.


Integration: Devo

Integration Version: 12

Device Product Field: Product Name

Event Name Field: context
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is ""|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.|False|.*|
|API Root|Specify API URL for the target Devo instance.|True|https://apiv2-us.devo.com|
|API Token|If token-based authentication is used, sSpecify API token for the target Devo instance.|False|*****|
|API Key|If access keys authentication is used, specify API key for the target Devo instance.|False|*****|
|API Secret|If access keys authentication is used, specify API secret for the target Devo instance.|False|*****|
|Verify SSL|If enabled, Siemplify server will check the certificate configured for API root.|False|false|
|Offset time in hours|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|24|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|30|
|Minimum Priority to Fetch|Minimum priority of the alert to be ingested to Siemplify, for example, Low or Medium. Possible values: Very low, Low, Normal, High, Very high.|False|4|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|

