# Connector_7_TenableIO
Pull vulnerabilities from Tenable.io. Note: connector works with plugin families in whitelist.


Integration: TenableIO

Integration Version: 18

Device Product Field: Product Name

Event Name Field: event_type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API Root of the Tenable.io instance.|True|https://cloud.tenable.com|
|Access Key|Access Key of the Tenable.io instance.|True|*****|
|Secret Key|Secret Key of the Tenable.io instance.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Tenable.io server is valid.|False|true|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch vulnerabilities. If nothing is provided, the connector will fetch all vulnerabilities. Possible values: Info, Low, Medium, High, Critical|False|Medium|
|Status Filter|Status filter for the connector. It works with comma-separated values. If nothing is provided, the connector will ingest vulnerabilities with "open", "reopened" statuses. Possible values: open, reopened, fixed.|False|open, reopened|
|Max Days Backwards|Number of days before the first connector iteration to retrieve vulnerabilities from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Default: 30 days. Note: this parameter will return vulnerabilities that were opened/reopened/fixed in the timeframe that is specified in "Max Days Backwards".|False|30|
|Grouping Mechanism|Grouping mechanism that will be used to create Siemplify Alerts. Possible values: Host, Vulnerability, None. If Host is provided, the connector will create 1 Siemplify alert containing all of the vulnerabilities per chunk related to the host. If Vulnerability is provided, the connector will create 1 Siemplify Alert containing information about all of the hosts that have that vulnerability in the scope of 1 chunk. If None or invalid value is provided, the connector will create a new Siemplify alert for each separate vulnerability per host.|True|Host|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

