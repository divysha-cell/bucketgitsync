# Connector_37_FortinetFortiSIEM
Connector can be used to fetch FortiSIEM incidents. Connector whitelist can be used to ingest only specific types of incidents based on incident’s “eventType” attribute value. SourceGroupIdentifier of the connector can be used to group Siemplify alerts based on incident id.  Connector requires FortiSIEM version 6.3 or newer.


Integration: FortinetFortiSIEM

Integration Version: 11

Device Product Field: deviceProduct

Event Name Field: eventType
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|Specify the API root for the target FortiSIEM installation.|True|https://127.0.0.1|
|Username|Specify the username to use for the target FortiSIEM installation.|True|dummy_valid_string|
|Password|Specify the password to use for the target FortiSIEM installation.|True|*****|
|Verify SSL|If enabled, Siemplify server will check the certificate configured for API root.|False|true|
|Target Organization|Specify organizations connector should fetch incidents for.|False|dummy_valid_string|
|Max hours backwards|Specify the time frame to fetch incidents from X hours backwards.|True|24|
|Max Incidents Per Cycle|Specify how many incidents should be processed during one connector run.|True|10|
|Max Events Per Incidents|Specify the maximum number of events the connector should track for the incident. Once the limit will be reached, new events will not be added to Siemplify.|True|100|
|Incident Statuses to Fetch|Specify incident' statuses to fetch to Siemplify. Parameter accepts multiple values as a comma separated string. 0 stands for incidents in open status.|False|0|
|Minimum Severity to Fetch|Specify minimum incident’s event severity to fetch to Siemplify in numbers, for example 5 or 7.|False|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Track New Events Added to Already Ingested Incidents|If enabled, if new events are added to already ingested FortiSIEM incident, additional new alert will be created in Siemplify that will have those new events.|False|true|
|Track New Events Threshold (hours)|If "Track New Events Added to Already Ingested Incidents" checkbox is checked, specify the maximum number of hours connector should track already ingested incidents for new events. Once the limit will be reached, new events will not be added to Siemplify.|True|24|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

