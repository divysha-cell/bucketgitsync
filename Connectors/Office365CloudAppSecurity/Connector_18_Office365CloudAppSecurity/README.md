# Connector_18_Office365CloudAppSecurity
Fetches alerts from Office 365 CloudApp Security.


Integration: Office365CloudAppSecurity

Integration Version: 27

Device Product Field: Not Supported

Event Name Field: description
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Alerts Padding Period|Time frame in minutes to search for new alerts backwards in time from the connector last run timestamp. Its recommended to adjust this value accordingly to the environment, for example 60 minutes.|False|0|
|Environment Field Name|Describes the name of the field where the environment name is stored.|False|dummy_valid_string|
|Environment Regex Pattern|If defined - the connector will implement the specific RegEx pattern on the data from "environment field" to extract specific string. For example - extract domain from sender's address: "(?<=@)(\S+$)"|False|10|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Cloud App Security portal URL|The URL of the Office 365 CloudApp Security portal.|True|https://127.0.0.1|
|API Token|API Token that will be used to authenticate with Office 365 CloudApp Security.|True|*****|
|Verify SSL|Verify SSL certificates for HTTPS requests to Office 365 CloudApp Security.|False|false|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run. Default: 5|True|5|
|Offset Time In Hours|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Default value: 24 hours.|True|24|

