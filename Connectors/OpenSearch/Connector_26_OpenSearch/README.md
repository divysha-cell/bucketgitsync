# Connector_26_OpenSearch
OpenSearch Connector


Integration: OpenSearch

Integration Version: 3

Device Product Field: device_product

Event Name Field: name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Server Address|The OpenSearch server address, i.e: http://{ip_address}:{port}|True|https://127.0.0.1|
|Username|OpenSearch username|False|dummy_valid_string|
|CA Certificate File|CA Certificate File|False|dummy_valid_string|
|Password|OpenSearch password|False|*****|
|JWT Token|OpenSearch JWT Token.|False|*****|
|Authenticate|Whether to authenticate on connection or not|False|FALSE|
|Verify SSL|Whether to use ssl on connection or not|False|FALSE|
|Alert Name Field|The name of the field where the alert name is as it appears in the OpenSearch UI. e.g. alert.info.name|True|dummy_valid_string|
|Timestamp Field|The name of the field where the timestamp is located as it appears in the OpenSearch UI. e.g. @timestamp|True|@timestamp|
|Environment Field|The name of the field where the environment is located is as it appears in the OpenSearch UI. e.g. host.environment|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is ''.|False|.*|
|Indexes|Index pattern to search by. e.g. '*'|True|*|
|Query|Search pattern query (Lucene query syntax). e.g. '*'|True|*|
|Alerts Count Limit|Max count of alerts to pull in one cycle. e.g. 20|True|20|
|Max Days Backwards|Max number of days to fetch alerts since. e.g. 3|True|1|
|Severity Field Name|If you want to map severity based on the string value then you would need to create a mapping file. Please refer to documentation portal for more details.|False|dummy_valid_string|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

