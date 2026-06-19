
# TrendVisionOne

Trend Vision One is a purpose-built threat defense platform that provides added value and new benefits beyond XDR solutions, allowing you to see more and respond faster. Providing deep and broad extended detection and response.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Trend Vision One instance.|True|String|https://{instance}|
|API Token|API Token of the Trend Vision One account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Trend Vision One server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Submit URL
Submit url in Trend Vision One. Supported entities: URL. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "url", "EntityResult": {"id": "3daefed8-466f-46c6-849a-4dd46edb94b4", "type": "url", "digest": {"md5": "f90a614c2ec8f72c55c2f50c0af923f3", "sha1": "d3f75803673b19c0c736efbaf6a8d3891ae18a10", "sha256": "3ba41b6e5c2ee4e9a2710976b177cf0db1080eb0277c554aa7d6ef1f0b04b33f"}, "analysisCompletionDateTime": "2023-10-16T17:38:21Z", "riskLevel": "noRisk", "detectionNames": [], "threatTypes": [], "trueFileType": "URL"}}]
```



#### Update Workbench Alert
Update a workbench alert in Trend Vision One.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|Specify what status to set for the alert.|True|List|Select One|
|Alert ID|Specify the ID of the alert needs to be updated.|True|String||



##### JSON Results
```json
{"schemaVersion": "1.14", "id": "WB-XXXXX-XXXXXXXX-XXXXX", "investigationStatus": "New", "workbenchLink": "https://portal.eu.xdr.trendmicro.com/index.html#/workbench?workbenchId=WB-XXXXX-XXXXXXXX-XXXXXX&ref=xxxxxxxxxx", "alertProvider": "XXX", "model": "[Heuristic Attribute] Possible OS Credential Dumping", "score": 24, "severity": "low", "createdDateTime": "2023-01-05T11:21:40Z", "updatedDateTime": "2023-03-13T11:39:13Z", "impactScope": {"desktopCount": 1, "serverCount": 0, "accountCount": 1, "emailAddressCount": 0, "entities": [{"entityType": "account", "entityValue": "windows10\\admin", "entityId": "windows10\\admin", "relatedEntities": ["XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX"], "relatedIndicatorIds": [], "provenance": ["Alert"]}, {"entityType": "host", "entityValue": {"guid": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", "name": "windows10", "ips": ["xxxx::xxxx:xxxx:xxxx:xxxx"]}, "entityId": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX", "relatedEntities": ["windows10\\admin"], "relatedIndicatorIds": [1, 2, 3, 4, 5, 6], "provenance": ["Alert"]}]}, "description": "Detects Possible Dumping of OS Information Technique", "matchedRules": [{"id": "xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx", "name": "[Heuristic Attribute] Possible OS Credential Dumping", "matchedFilters": [{"id": "xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx", "name": "Demo - Possible Credential Dumping via Registry Hive", "matchedDateTime": "2023-01-05T11:20:01.957Z", "mitreTechniqueIds": ["V9.T1003.002", "T1003"], "matchedEvents": [{"uuid": "216ec125-8115-4263-b3a7-54a7a31e994a", "matchedDateTime": "2023-01-05T11:20:01.957Z", "type": "TELEMETRY_PROCESS"}]}]}], "indicators": [{"id": 1, "type": "command_line", "field": "objectCmd", "value": "cmd.exe  /c echo \"reg.exe save hklm\\sam C:\\trend-micro-test\\trend-micro-test.hive\"", "relatedEntities": ["XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXX"], "filterIds": ["xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxx"], "provenance": ["Alert"]}, {"id": 2, "type": "command_line", "field": "processCmd", "value": "C:\\Windows\\SYSTEM32\\cmd.exe /c \"C:\\Users\\Admin\\Documents\\TrendMicroVisionOne\\T1003_Demo_Script.bat\"", "relatedEntities": ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX"], "filterIds": ["xxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx"], "provenance": ["Alert"]}, {"id": 3, "type": "command_line", "field": "parentCmd", "value": "C:\\Windows\\system32\\svchost.exe -k netsvcs -p -s Schedule", "relatedEntities": ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"], "filterIds": ["xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx"], "provenance": ["Alert"]}, {"id": 4, "type": "file_sha256", "field": "processFileHashSha256", "value": "B99D61D874728EDC0918CA0EB10EAB93D381E7367E377406E65963366C874450", "relatedEntities": ["XXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX"], "filterIds": ["xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx"], "provenance": ["Alert"]}, {"id": 5, "type": "fullpath", "field": "processFilePath", "value": "C:\\Windows\\System32\\cmd.exe", "relatedEntities": ["XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX"], "filterIds": ["xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx"], "provenance": ["Alert"]}, {"id": 6, "type": "text", "field": "endpointHostName", "value": "WINDOWS10", "relatedEntities": ["XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX"], "filterIds": ["xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxx"], "provenance": ["Alert"]}]}
```



#### Execute Email
Execute email action on the endpoint in Trend Vision One. Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Action|Specify the action for the email.|False|List|Delete|
|Message ID|Specify the ID of the message that needs to be used in the action.|True|String||
|Mailbox|Specify the mailbox related to the message.|False|String||
|Description|Specify a description for the performed action.|False|String||



##### JSON Results
```json
{"id": "RM-20231017-00001", "status": "running", "createdDateTime": "2023-10-17T05:25:37Z", "lastActionDateTime": "2023-10-17T05:25:37Z", "description": "task description", "action": "quarantineMessage", "account": "API key", "tasks": [{"messageId": "<64e32256-fae1-4652-9f7a-8e514ec86d5a@az.northcentralus.microsoft.com>", "mailBox": "james.bond@siemplifycyarx.onmicrosoft.com", "messageSubject": "Microsoft 365 Defender has merged the incidents detected in your environment", "uniqueId": "AAkALgAAAAAAHYQDEapmEc2byACqAC-EWg0A28vWY1XUyUyUUvI8a3APqAADxR_EPAAA", "organizationId": "40c52b8c-062a-4095-bd74-e46a5eb48308", "status": "running", "lastActionDateTime": "2023-10-17T05:25:38Z"}]}
```



#### Submit File
Submit file in Trend Vision One. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|Specify a comma-separated list of paths for the files that need to be submitted.|True|String||
|Archive Password|Specify the password for the archive.|False|Password|*****|
|Document Password|Specify the password for the document.|False|Password|*****|
|Arguments|Specify the arguments for the submitted file.|False|String||



##### JSON Results
```json
[{"Entity": "file path", "EntityResult": {"id": "3daefed8-466f-46c6-849a-4dd46edb94b4", "type": "file", "digest": {"md5": "f90a614c2ec8f72c55c2f50c0af923f3", "sha1": "d3f75803673b19c0c736efbaf6a8d3891ae18a10", "sha256": "3ba41b6e5c2ee4e9a2710976b177cf0db1080eb0277c554aa7d6ef1f0b04b33f"}, "analysisCompletionDateTime": "2023-10-16T17:38:21Z", "riskLevel": "noRisk", "detectionNames": [], "threatTypes": [], "trueFileType": "Shell Script"}}]
```



#### Ping
Test connectivity to the Trend Vision One with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Unisolate Endpoint
Unisolate endpoints in Trend Vision One. Supported entities: IP Address, Hostname. Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Description|Specify the reasoning for the unisolation of the endpoints.|False|String||
|Agent UUID|A comma-separated list of UUIDs. The action processes these UUIDs along with their related entities.|False|String||



##### JSON Results
```json
[{"Entity": "172.xx.xxx.xxx", "EntityResult": {"task_id": "1", "status": "succeeded"}}]
```



#### Isolate Endpoint
Isolate endpoints in Trend Vision One. Supported entities: IP Address, Hostname. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Description|Specify the reasoning for the isolation of the endpoints.|False|String||
|Agent UUID|A comma-separated list of UUIDs. The action processes these UUIDs along with their related entities.|False|String||



##### JSON Results
```json
[{"Entity": "172.xx.xxx.xxx", "EntityResult": {"task_id": "1", "status": "succeeded"}}]
```



#### Enrich Entities
Enrich entities using information from Trend Vision One. Supported entities: Hostname, IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Agent UUID|A comma-separated list of UUIDs. The action processes these UUIDs along with their related entities.|False|String||



##### JSON Results
```json
[{"Entity": "172.xx.xxx.xxx", "EntityResult": {"agentGuid": "3573fxxx-xxxx-xxxx-xxxx-xxxxxxxx", "osName": "Linux", "osVersion": "CentOS 7", "osDescription": "CentOS 7 (64 bit) (3.10.0-1160.80.1.el7.x86_64)", "productCode": "xes", "loginAccount": {"value": [], "updatedDateTime": ""}, "endpointName": {"value": "trend-visionone-centos7", "updatedDateTime": "2023-03-06T10:24:42.000Z"}, "macAddress": {"value": ["02:xx:xx:xx:xx:xx", "00:xx:xx:xx:xx:xx"], "updatedDateTime": "2023-03-06T10:24:42.000Z"}, "ip": {"value": ["172.xx.xxx.xx"], "updatedDateTime": "2023-03-06T10:24:42.000Z"}, "installedProductCodes": ["xes"]}}]
```



#### Execute Custom Script
Execute custom script on the endpoint in Trend Vision One. Supported entities: Hostname, IP address. Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Script Name|Specify the name of the script that needs to be executed on the endpoints.|True|String||
|Script Parameters|Specify the parameters for the script.|False|String||
|Agent UUID|A comma-separated list of UUIDs. The action processes these UUIDs along with their related entities.|False|String||



##### JSON Results
```json
[{"Entity": "172.xx.xxx.xxx", "EntityResult": {"task_id": "1", "status": "succeeded"}}]
```









## Connectors
#### Trend Vision One - Workbench Alerts Connector
Pull information about workbench alerts from Trend Vision One. Note: dynamic list filter works with "model" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field through regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Trend Vision One instance.|True|String|https://{instance}|
|API Token|API Key of the Trend Vision One account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Trend Vision One server is valid.|False|Boolean|true|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch alerts. Possible values: Low, Medium, High, Critical. If nothing is specified, the connector will ingest alerts with all severities.|False|String||
|Max Hours Backwards|Amount of hours from where to fetch alerts.|False|Int|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Default: 10.|False|Int|10|
|Use dynamic list as a blocklist|If enabled, dynamic lists will be used as a blocklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




