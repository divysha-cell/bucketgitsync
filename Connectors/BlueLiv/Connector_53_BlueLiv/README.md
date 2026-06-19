# Connector_53_BlueLiv
Pull security threats from BlueLiv. Connector fetches all of the latest threats from BlueLiv modules. Whitelist and blacklist filters work with BlueLiv module types. For example, if you want to get threats only from Hacktivism modules, you can turn on the whitelist and type in the Hacktivism type name.


Integration: BlueLiv

Integration Version: 14

Device Product Field: Product Name

Event Name Field: event_type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Analysis Results To Ingest|Filter the threats by the analyst analysis to this threat, only ingest threats with the chosen analysis result. Provide a comma separated list of the desired analysis results to ingest. Possible values: NOT_AVAILABLE, NOT_IMPORTANT, NOT_PROCESSABLE, POSITIVE, NEGATIVE, INFORMATIVE, IMPORTANT.|False|dummy_valid_string|
|Labels To Filter By|Please provide a comma separated list of the label names you want to filter by. Please pay attention to uppercase and lowercase letters and write the labels exactly as they appear in BlueLiv UI.|False|dummy_valid_string|
|Reading Status To Ingest|Filter the threats by their reading status, so that the connector will ingest according to it. If no value is provided we will fetch both. Options:  “Only Read”, “Only Unread”.|False|dummy_valid_string|
|Should ingest only starred threats?|If checked, only starred (favorite) threats will be ingested.|False|false|
|Should ingest threats related to incidents?|Should connector filter the threats by checking the relationship to an incident. If no value is provided we will fetch both. Options are: Only Incidents - will ingest only threats related to incidents, Only Non Incidents - will ingest only threats that are not related to incidents.|False|dummy_valid_string|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Severity|Severity will be one from the following values Low, Medium, High, Critical. Will be assigned to Siemplify alerts created from this connector.|True|Medium|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API URL|API Root of the BlueLiv instance.|True|https://example.blueliv.com/|
|User Name|User name for BlueLiv.|True|dummy_valid_string|
|Password|User password for BlueLiv.|True|*****|
|Organization ID|Specify the Organization ID to use in BlueLiv.|True|dummy_valid_string|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the BlueLiv server is valid.|False|false|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Threats To Fetch|How many threats to process per one connector iteration. Note - Maximum value here is 100.|False|10|

