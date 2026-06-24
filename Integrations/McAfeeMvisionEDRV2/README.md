
# McAfeeMvisionEDRV2

McAfee MVISION Endpoint Detection and Response (MVISION EDR) is a cloud-delivered service that enables you to detect advanced device threats, fully investigate, and quickly respond. Continuous data collection and advanced analytics detect suspicious behavior.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|URL|https://api.mvision.mcafee.com|
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|API Key|None|True|Password|*****|
|Scopes|None|True|String|epo.device.r epo.device.w epo.evt.r epo.taggroup.r epo.taggroup.w epo.tags.r epo.tags.w mi.user.investigate soc.inv.ade|
|IAM Root|None|True|URL|https://iam.mcafee-cloud.com|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|TIPCommon-1.0.10-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|


## Actions
#### Create Investigation
Create investigations for IP addresses and hostnames.
Timeout - 300 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Type|Defines the type of alert.|True|List|IOC|
|Priority|Assigns a priority to the investigation.|True|List|Low|
|Hint|Automatically links related investigations and avoids creating many cases from multiple alerts related to the same incident. If the same hint is used, the evidences will be added to the already existing investigation.|False|String||
|Name|Gives the investigation a meaningful name. If the name is missing, a default case name is assigned.|False|String||



##### JSON Results
```json
[{"Entity": "1.1.1.1", "EntityResult": {"type": "investigations", "id": "05cae9b0-24ca-11eb-b713-000000000000", "attributes": {"created": "2020-11-12T09:32:46.411Z", "lastModified": "2020-11-12T09:32:46.411Z", "name": "Siemplify Test", "owner": "unknown", "summary": "", "source": "unknown", "isAutomatic": true, "hint": "Test", "caseType": "IOC", "investigated": true, "status": "In progress", "priority": "High"}}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









