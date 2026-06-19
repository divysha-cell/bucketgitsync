# Connector_4_VaronisDataSecurityPlatform
Connector can be used to fetch alerts from the Varonis Data Security Platform. The connector dynamic list can be used to filter specific alerts for ingestion based on the Varonis Data Security Platform alert name.


Integration: VaronisDataSecurityPlatform

Integration Version: 7

Device Product Field: device_product

Event Name Field: Type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the event field where the environment name is stored.
If the environment field isn't found, the environment is "".|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.
Default is .* to catch all and return value unchanged.
Used to allow the user to manipulate the environment field through regex logic
If the regex pattern is null or empty, or the environment value is null, the final environment result is "".|False|.*|
|API Root|Specify the API URL for the target Varonis Data Security Platform instance.|True|https://127.0.0.1|
|Username|Specify the username to connect with.|True|dummy_valid_string|
|Password|Specify the password to connect with.|True|*****|
|Verify SSL|If enabled, the certificate configured for the API root is validated.|False|false|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|3|
|Max Alerts per Cycle|Fetch X alerts per connector cycle.|True|10|
|Max Events per Varonis alert|Maximum number of events that the connector fetches for the Data Security Platform alert.|True|25|
|Status|Data Security Platform alert statuses to fetch.|True|Open, Under Investigation, Closed|
|Severity|Data Security Platform alert severities to fetch.|True|Low, Medium, High|
|Disable Overflow|If enabled, the connector ignores the Chronicle SOAR overflow mechanism when creating alerts.|False|false|
|Use Dynamic List as BlockList|If enabled, the connector uses alert names specified in the Dynamic list as a BlockList. It ingests only alerts that don't match Dynamic List.|False|false|
|Alert Name Template|If provided, the connector uses this value for Chronicle SOAR Alert Name. Please refer to the documentation portal for more details. You can provide placeholders in the following format: [name of the field]. Example: Varonis alert - [name]. Note: The connector first uses CSOAR Event for placeholders. Only keys that have string value are handled. If nothing is provided or the user provides an invalid template, the connector uses the default alert name - [name].|False|[Name]|
|Rule Generator Template|If provided, the connector uses this value for Chronicle SOAR Rule Generator Value. Please refer to the documentation portal for more details. You can provide placeholders in the following format: [name of the field]. Example: Varonis alert - [name]. Note: The connector first uses Chronicle SOAR Event for placeholders. Only keys that have string value are handled. If nothing is provided or the user provides an invalid template, the connector uses the default rule generator - [name].|False|[Name]|
|Proxy Server Address|Proxy server to use for connection to the mail server.|False|https://127.0.0.1|
|Proxy Username|Proxy server username|False|dummy_valid_string|
|Proxy Password|Proxy server password|False|*****|

