# Qualys EDR - Events Connector_18
Pull information about events from Qualys EDR.


Integration: QualysEDR

Integration Version: 5.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|API Root|API root of the Qualys EDR instance.|True|http://x.x.x.x|
|Username|Username of the Qualys EDR account.|True|0|
|Password|Password of the Qualys EDR account.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Qualys EDR server is valid.|False|true|
|Lowest Score To Fetch|Lowest Score that needs to be used to fetch events.  Maximum: 10. If nothing is specified, connector will ingest events with all scores.|False|5|
|Type Filter|Type filter for the events. Possible values: File,mutex,process,network,registry.|True|file, network|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Events To Fetch|How many alert logs to process per one connector iteration. Default: 100.|False|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|

