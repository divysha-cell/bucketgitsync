
# ProofpointCloudThreatResponse

Proofpoint Threat Response includes a cloud-based security solution that runs in Proofpoint's cloud infrastructure as part of Threat Response's suite of products. It acts on email messages with identified malicious URLs, attachments and BEC (Business Email Compromise) threats. Threat Response removes such emails from the user's mailboxes, and subsequently from any mailboxes to which they were forwarded.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The API Root of the Proofpoint Cloud Threat Response instance.|True|String|https://threatprotection-api.proofpoint.com|
|Client ID|The Client ID of the Proofpoint Cloud Threat Response instance.|True|String||
|Client Secret|The Client Secret of the Proofpoint Cloud Threat Response instance.|True|Password|*****|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to the Proofpoint Cloud Threat Response server. Enabled by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|proto_plus-1.27.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pyparsing-3.2.5-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|anyio-4.12.0-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|httplib2-0.31.0-py3-none-any.whl|
|certifi-2025.11.12-py3-none-any.whl|
|cachetools-6.2.4-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|google_api_core-2.28.1-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_api_python_client-2.187.0-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|cryptography-46.0.3-cp311-abi3-manylinux_2_34_x86_64.whl|
|urllib3-2.6.2-py3-none-any.whl|
|google_auth-2.45.0-py2.py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|protobuf-6.33.2-cp39-abi3-manylinux2014_x86_64.whl|
|pycparser-2.23-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|TIPCommon-2.2.19-py2.py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|


## Actions
#### Ping
Use the Ping action to test the connectivity to Proofpoint Cloud Threat Response.
Timeout - 600 Seconds









## Connectors
#### Proofpoint Cloud Threat Response - Incidents Connector
Pull incidents from Proofpoint Cloud Threat Response. Dynamic List works with the "sourceTypes" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The name of the field where the product name is stored.|True|String|Product Name|
|EventClassId|The name of the field that determines the event name (subtype).|True|String|product|
|Environment Field Name|The name of the field where the environment name is stored. If no value is provided, the connector uses the default environment.|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the Environment Field Name field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value .* to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|The timeout limit, in seconds, for the Python process that runs the current script.|True|Integer|180|
|API Root|The API Root of the Proofpoint Cloud Threat Response instance.|True|String|https://threatprotection-api.proofpoint.com|
|Client ID|The Client ID of the Proofpoint Cloud Threat Response instance.|True|String||
|Client Secret|The Client Secret of the Proofpoint Cloud Threat Response instance.|True|Password|*****|
|Lowest Severity To Fetch|The lowest severity of the alerts to retrieve. The possible values are as follows:: High, Medium, Low. If no value is provided, the connector ingests alerts with all severity levels.|False|String||
|Status Filter|The status filter for the ingestion of incidents. The possible values are Open, Closed.|False|String|Open|
|Lowest Confidence To Fetch|The confidence filter for the ingestion of incidents. The possible values are High, Medium, Low. If no value is provided, this filter is not applied.|False|String||
|Disposition Filter|The disposition filter for the ingestion of incidents. The possible values are: Bulk, Clean, Impostor, In Progress, Internal, Low Risk, Malware, Manual Review, Not Set, Phish, Scam, Simulated Phish, Spam, Suspicious, Tap False Positive, Toad, Vendor|False|String||
|Verdict Filter|The verdict filter for the ingestion of incidents. The possible values are Failed, Low Risk, Manual Review, Threat.|False|String||
|Max Hours Backwards|The number of hours prior to now to retrieve alerts. This parameter can apply to the initial connector iteration after you enable the connector for the first time, or the fallback value for an expired connector timestamp.|True|Integer|1|
|Max Incidents To Fetch|The number of incidents to process in every connector iteration. Max: 9.|True|Integer|9|
|Use dynamic list as a blocklist|If selected, the connector uses the dynamic list as a blocklist.|False|Boolean|false|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism.|False|Boolean|false|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to the Proofpoint Cloud Threat Response server.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




