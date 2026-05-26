# Anomali Staxx - Indicators Connector
Pull indicators from Anomali Staxx


Integration: AnomaliStaxx

Integration Version: 5.0

Device Product Field: fProduct Name

Event Name Field: itype
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|Username|Username of the Anomali Staxx account.|True|b|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False||
|Server Address|Server address of the Anomali Staxx instance.|True|https://<ip>:<port>|
|Password|Password of the Anomali Staxx account.|True|*****|
|Server Timezone|Specify which timezone is set on the Anomali Staxx server in regards to UTC. For example, +1, -1, etc. If nothing is specified, the connector will use UTC as a default timezone.|False||
|Lowest Severity To Fetch|Lowest severity that will be used to fetch incidents. Possible values: Low, Medium, High, Critical.|True|Medium|
|Lowest Confidence To Fetch|Lowest confidence that will be used to fetch indicators.|False|0|
|Fetch Max Hours Backwards|Amount of hours from where to fetch indicators.|False|1|
|Max Indicators To Fetch|How many indicators to process per one connector iteration.|False|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Anomali Staxx server is valid.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False|*****|


Addon !@12