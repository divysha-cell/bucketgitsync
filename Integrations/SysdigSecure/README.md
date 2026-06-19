
# SysdigSecure

Sysdig Secure is a comprehensive security platform that provides continuous security and compliance monitoring for cloud-native environments.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The API root of the Sysdig Secure instance.|True|String||
|API Token|The Sysdig Secure API token.|True|Password|*****|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to Sysdig Secure. Selected by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|proto_plus-1.25.0-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|TIPCommon-2.0.7-py2.py3-none-any.whl|
|protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|httpcore-1.0.5-py3-none-any.whl|
|google_api_core-2.22.0-py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|anyio-4.4.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|google_auth-2.35.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|google_api_python_client-2.151.0-py2.py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Ping
Use the Ping action to test the connectivity to Sysdig Secure.
Timeout - 600 Seconds









## Connectors
#### Sysdig Secure - Events Connector
Use the Sysdig Secure - Events Connector to pull events from Sysdig Secure. The dynamic list works with the "ruleName" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment.|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the Environment Field Name field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value .* to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|The API root of the Sysdig Secure instance.|True|String||
|API Token|The Sysdig Secure API token.|True|Password|*****|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to Sysdig Secure|False|Boolean|false|
|Lowest Severity To Fetch|The lowest severity of the events to fetch. If you don't set a value, the connector ingests events with all severities. The possible values are as follows: Informational, Low, Medium, High.|False|String||
|Custom Filter Query|A query to filter, scope, or group events during ingestion. This parameter has priority over the "Lowest Severity To Fetch" parameter and values that you provide in the dynamic list. For more information about how to filter events, see Filter Secure Events (https://docs.sysdig.com/en/docs/sysdig-secure/threats/activity/events-feed/#filter-secure-events). Example: host.hostName = "instance-1"|False|String||
|Max Hours Backwards|A number of hours before the first connector iteration to retrieve the events from. This parameter can apply to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp.|True|Int|1|
|Max Events To Fetch|The maximum number of events to process for every connector iteration. The maximum value is 200.|True|Int|100|
|Use dynamic list as a blocklist|If enabled, the dynamic list will be used as a blocklist.|False|Boolean|false|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




