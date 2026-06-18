# Splunk ES - Notable Events Connector_13
Ingest notable events from Splunk ES. Note: This connector only works with Splunk ES.


Integration: Splunk

Integration Version: 65.0

Device Product Field: dummy_device

Event Name Field: dummy_event
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|0|
|Environment Regex Pattern|A regex pattern to run on the value found in the 'Environment Field Name' field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|Rule Generator Field Name|The name of the field that will be used to map the rule generator value. Note: only information about notable event itself is used for mapping, events are disregarded. If invalid value is provided, connector will use "rule_name" as field.|False|0|
|Server Address|Server address of the Splunk instance.|True|https://<ip>:8089|
|Username|Username of the Splunk account.|False|0|
|Password|Password of the Splunk account.|False|*****|
|API Token|Splunk API token. API token has priority over other authentication methods, when this field is not empty.|False|*****|
|Lowest Urgency To Fetch|Lowest urgency that will be used to fetch notable events. Possible values: Informational Low Medium High Critical|True|Medium|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve notable events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Padding Time|Amount of hours that will be used as a padding. If nothing is provided, this parameter is not going to be applied. Max 100 hours. Note: it's not safe to increase the padding period beyond 12 hours.|False|0|
|Only Drilldown Events|If enabled, the connector will only try to fetch drilldown events, without trying to fetch base events. Note: this parameter requires 'Extract Base Events' to be enabled.|False|false|
|Max Notable Events To Fetch|How many notable events to process per one connector iteration.|False|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Splunk server is valid.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|0|
|Proxy Username|The proxy username to authenticate with.|False|0|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Query Filter|Additional filter for the query that is sent to Splunk to get notable events. Value provided here will be appended to the WHERE clause of the query. Please refer to documentation portal for more information.|False|0|
|CA Certificate File|CA Certificate File|False|0|
|Extract Base Events|If enabled, connector will try to extract base events related to notable event using information about the job. In other case, connector will create a Siemplify Event based on the notable event. Note: that if parameter is set to True, but connector can't work with jobs, connector will use information about notable event as a fallback mechanism.|False|true|
|Notable Event Data Along Base Event|If enabled, connector will create Siemplify Events based on both Notable Event and Base Events together.|False|false|
|Multivalue Fields|A comma-separated list of fields that contain multiple entities. If, for example, one field can contain two hostnames, we would need to split notable event into two Siemplify Events in order to do a correct mapping of entities.|False|asset, src, dest, ip|
|Alert Name Source|Source for the alert name. Possible values: Search Name, Rule Name.|False|Search Name|

