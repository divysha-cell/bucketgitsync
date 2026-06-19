# Connector_32_PaloAltoPrismaCloud
Pull alerts from Palo Alto Prisma Cloud. Dynamic List works with the “policy.name” parameter.


Integration: PaloAltoPrismaCloud

Integration Version: 6

Device Product Field: policy_policyType

Event Name Field: resource_cloudType
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored.If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged.Used to allow the user to manipulate the environment field via regex logic.If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Palo Alto Prisma Cloud instance.|True|https://api3.prismacloud.io|
|Access Key ID|Access key ID of the Palo Alto Prisma Cloud account.|True|dummy_valid_string|
|Secret Access Key|Secret access key of the Palo Alto Prisma Cloud account.|True|*****|
|Lowest Severity To Fetch|Lowest severity of the alerts to fetch. If no value is provided, the connector ingests alerts with all severities.Possible values: Critical, High, Medium, Low, Informational|False|dummy_valid_string|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alerts To Fetch|Number of alerts to process per one connector iteration. Max value is 1000. Default value is 100.|False|100|
|Use dynamic list as a blocklist|If checked, the dynamic list is used as a blocklist.|False|false|
|Verify SSL|If checked, verifies that the SSL certificate for the connection to the Palo Alto Prisma Cloud server is valid.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

