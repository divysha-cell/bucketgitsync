# Connector_39_Fortigate
Pull information about different threat logs from Fortigate. Note: whitelist filter works with "eventtype" parameter.


Integration: Fortigate

Integration Version: 20

Device Product Field: Product Name

Event Name Field: eventtype
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Fortigate instance.|True|https://127.0.0.1|
|API Key|API key of the Fortigate account.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Fortigate server is valid.|False|true|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|true|
|Lowest Security Level To Fetch|Lowest security level that needs to be used to fetch threat logs. Possible values: debug, information, notice, warning, error, critical, alert, emergency. If nothing is specified, the connector will ingest threat logs with all security levels.|False|warning|
|Threat Log Location|Location of the threat log.|False|dummy_valid_string|
|Threat Subtypes To Fetch|A comma-separated list of threat subtypes to ingest. The possible values are as follows:virus, webfilter, waf, ips, anomaly, app-ctrl, emailfilter, dlp, voip, gtp, dns, ssh, ssl, cifs, file-filter, traffic/local, traffic/forward.|True|virus, webfilter, waf, ips, anomaly, file-filter|
|VDOM|The Virtual Domain (VDOM) name to target within the FortiGate device.|False|dummy_valid_string|
|Serial Number|The serial number of the FortiGate device.|False|dummy_valid_string|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve threat logs from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration per subtype. Default: 100.|False|20|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

