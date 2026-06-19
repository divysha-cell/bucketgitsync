# Connector_54_AmazonMacie
Pull findings from Amazon Macie. Note: Whitelist works with Finding types, for example, SensitiveData:S3Object/Personal.


Integration: AmazonMacie

Integration Version: 11

Device Product Field: Product Name

Event Name Field: Type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|AWS Access Key ID|AWS Access Key ID to use in integration.|True|dummy_valid_string|
|AWS Secret Key|AWS Secret Key to use in integration.|True|*****|
|AWS Default Region|AWS default region to use in integration, for example us-west-2.|True|dummy_valid_string|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve findings from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max findings to fetch|How many findings to process per one connector iteration.|False|50|
|Finding severity to ingest|Finding severity to ingest - High, Medium or Low. Parameter accepts multiple values as a comma separated string. If nothing is specified - ingest all findings regardless of severity.|False|dummy_valid_string|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

