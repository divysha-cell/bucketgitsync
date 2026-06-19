# Connector_16_Site24x7
Pull information about alert logs from Site24x7.


Integration: Site24x7

Integration Version: 8

Device Product Field: Product Name

Event Name Field: eventType
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|API root of the Site24x7 instance. Possible api roots:
 United States
 https://www.site24x7.com
 Europe
 https://www.site24x7.eu
 China
 https://www.site24x7.cn
 India
 https://www.site24x7.in
 Australia
 https://www.site24x7.net.au|True|https://127.0.0.1|
|Refresh Token|Site24x7 Refresh token. You can generate this token using action "Get Refresh Token".|True|*****|
|Client ID|Client ID of the Site24x7 instance.|True|dummy_valid_string|
|Client Secret|Client Secret of the Site24x7 instance.|True|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Site24x7 server is valid.|False|true|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alert logs from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Max Alert Logs To Fetch|How many alert logs to process per one connector iteration. Default: 100.|False|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

