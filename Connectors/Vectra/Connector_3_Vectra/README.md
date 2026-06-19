# Connector_3_Vectra
Vectra - Detections Connector


Integration: Vectra

Integration Version: 14

Device Product Field: Product Name

Event Name Field: detection_detection_category
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Vectra server.|True|https://127.0.0.1|
|API Token|API token of the Vectra account.|True|*****|
|Lowest Threat Score To Fetch|Lowest threat score that will be used to fetch detections. Min:0 Max:100|True|50|
|Lowest Certainty Score To Fetch|Lowest certainty score that will be used to fetch detections. Min: 0 Max: 100|False|0|
|Category Filter|Specify which categories of detections to ingest into Siemplify. Possible values: Command & Control  Botnet  Reconnaissance  Lateral Movement  Exfiltration  Info|False|Command & Control, Botnet, Reconnaissance, Lateral Movement, Exfiltration, Info|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve threats from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Detections To Fetch|How many detections to process per one connector iteration. Limit is 5000. This is a Vectra limitation.|False|25|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Vectra server is valid.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

