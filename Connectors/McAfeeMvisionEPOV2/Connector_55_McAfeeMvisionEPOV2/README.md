# Connector_55_McAfeeMvisionEPOV2
Pull events from McAfee Mvision EPO V2.


Integration: McAfeeMvisionEPOV2

Integration Version: 9

Device Product Field: Product Name

Event Name Field: threattype
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|True|50|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the CheckPoint Cloud Guard server is valid.|False|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|API Root|API Root of the McAfee Mvision EPO V2 account.|True|https://api.mvision.mcafee.com|
|IAM Root|IAM Root of the McAfee Mvision EPO V2 API.|True|https://iam.mcafee-cloud.com|
|Client ID|Client ID of the McAfee Mvision EPO V2 account.|True|dummy_valid_string|
|Client Secret|Client Secret of the McAfee Mvision EPO V2 account.|True|*****|
|API Key|API Key of the McAfee Mvision EPO V2 account.|True|*****|
|Scopes|Scopes of the McAfee Mvision EPO V2 account.|False|epo.device.r epo.device.w epo.evt.r epo.taggroup.r epo.taggroup.w epo.tags.r epo.tags.w mi.user.investigate soc.inv.ade|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|

