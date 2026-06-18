# Qualys VM - Detections Connector_20
Pull detections from Qualys VM. Note: whitelist works with "Type" parameter.


Integration: QualysVM

Integration Version: 28.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|API Root|API Root of the Qualis VM instance.|True|0|
|Username|Username of the Qualis VMDR instance.|True|0|
|Password|Password of the Qualis VMDR instance.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Qualys VM server is valid.|False|true|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch detections. If nothing is provided, the connector will fetch all detections. Maximum: 5.|False|1|
|Status Filter|Status filter for the connector. If nothing is provided, the connector will ingest detections with "New, Active, Re-Opened" statuses. Possible values: NEW, ACTIVE, FIXED, RE-OPENED.|False|NEW, ACTIVE, RE-OPENED|
|Ingest Ignored Detections|If enabled, the connector will ingest ignored detections.|False|false|
|Ingest Disabled Detections|If enabled, the connector will ingest disabled detections.|False|false|
|Grouping Mechanism|Grouping mechanism that will be used to create Siemplify Alerts. Possible values: Host, Detection, None. If Host is provided, the connector will create 1 Siemplify alert containing all of the detection related to the host. If Detection is provided, the connector will create 1 Siemplify Alert containing information about all of the hosts that have that detection. If None or invalid value is provided, the connector will create a new Siemplify alert for each separate detection per host.|True|Detection|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|X-Requested-With Header|On behalf of whom, the API requests need to be executed in the integration|True|Google SecOps SOAR|

