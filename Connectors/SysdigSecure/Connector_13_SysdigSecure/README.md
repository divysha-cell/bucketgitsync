# Connector_13_SysdigSecure
Use the Sysdig Secure - Events Connector to pull events from Sysdig Secure. The dynamic list works with the "ruleName" parameter.


Integration: SysdigSecure

Integration Version: 2

Device Product Field: Product Name

Event Name Field: content_ruleName
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regular expression pattern to run on the value found in the Environment Field Name field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value .* to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|The API root of the Sysdig Secure instance.|True|https://127.0.0.1|
|API Token|The Sysdig Secure API token.|True|*****|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to Sysdig Secure|False|false|
|Lowest Severity To Fetch|The lowest severity of the events to fetch. If you don't set a value, the connector ingests events with all severities. The possible values are as follows: Informational, Low, Medium, High.|False|dummy_valid_string|
|Custom Filter Query|A query to filter, scope, or group events during ingestion. This parameter has priority over the "Lowest Severity To Fetch" parameter and values that you provide in the dynamic list. For more information about how to filter events, see Filter Secure Events (https://docs.sysdig.com/en/docs/sysdig-secure/threats/activity/events-feed/#filter-secure-events). Example: host.hostName = "instance-1"|False|3|
|Max Hours Backwards|A number of hours before the first connector iteration to retrieve the events from. This parameter can apply to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp.|True|1|
|Max Events To Fetch|The maximum number of events to process for every connector iteration. The maximum value is 200.|True|100|
|Use dynamic list as a blocklist|If enabled, the dynamic list will be used as a blocklist.|False|false|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

