
# Tanium

Tanium is a feature-packed endpoint management and endpoint security platform designed to strengthen and optimize an organization’s cybersecurity efforts. The platform gives security teams the tools they need to fortify existing security gaps or completely overhaul their cybersecurity environments, providing complete threat response capabilities from a single endpoint agent. Encompassing everything from asset and threat discovery to complete threat response capabilities from a single endpoint agent, Tanium gives security teams the tools they need to fortify existing security gaps and/or completely overhaul their cyber security environments to adequately prepare themselves for future generations of cyber threats.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String||
|API Token|None|True|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|idna-3.8-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|


## Actions
#### Delete File
Download a file from endpoints in Tanium. Action works with Tanium Threat Response API. Supported Entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|Specify the absolute path of the files on the endpoint that needs to be deleted.|True|String||



##### JSON Results
```json
[{"Entity":"centos-xxx.xxx.xxx","EntityResult":{"success":["filepath1"],"not_exist_already_or_errors":["invalid.jar","badfile.txt"]}},{"Entity":"172.30.xxx.xxx","EntityResult":{"success":["filepath1"],"not_exist_already_or_errors":["invalid.jar","badfile.txt"]}}]
```



#### Ping
Test connectivity to the Tanium installation with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### List Connections
List endpoint connections in Tanium.
Timeout - 600 Seconds



##### JSON Results
```json
[{"sessionId":null,"ip":"172.xx.xxx.xxx","hostname":"hostname.lab.local","clientId":"1122334455","platform":"Windows","eid":"0000","initiatedAt":1710744548166,"status":"timeout","message":"The connection has timed out.","userId":"000","personaId":0,"id":"remote:hostname.lab.local:1122334455:0000"}]
```



#### Quarantine Endpoint
Quarantine the endpoints in Tanium. Action works with Tanium Threat Response API. Supported Entities: Hostname, IP Address. Note: Action is running as async, if "Only Initiate" is set to false, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Only Initiate|If enabled, action will only initiate the task execution without waiting for results.|False|Boolean|false|
|Package Names|Specify a JSON object containing all of the package names for each OS.|True|String|{"Linux":"Apply Linux IPTables Quarantine","Mac":"Apply Mac PF Quarantine","Windows":"Apply Windows IPsec Quarantine"}|
|Package Parameters|Specify a JSON object containing all of the parameters for the package being deployed. If nothing is provided, action will use the following payload: [{"key":"$1","value":null},{"key":"$2","value":null},{"key":"$3","value":null},{"key":"$4","value":null},{"key":"$5","value":null},{"key":"$6","value":null},{"key":"$7","value":null},{"key":"$8","value":null},{"key":"$9","value":null}]|False|String||



##### JSON Results
```json
[{"Entity":"centos-xxxx","EntityResult":{"id":417,"type":"responseAction","status":"COMPLETED","metadata":{"id":7,"type":"quarantine","status":"QUEUED","computerName":"centos-xxxx","userId":1,"userName":"tanium","options":{"packageName":"Apply Linux IPTables Quarantine","packageParameters":[{"key":"$1","value":null},{"key":"$2","value":null},{"key":"$3","value":null},{"key":"$4","value":null},{"key":"$5","value":null},{"key":"$6","value":null},{"key":"$7","value":null},{"key":"$8","value":null},{"key":"$9","value":null}],"packageSkipLockFlag":false},"results":{},"expirationTime":"1970-01-01T00:09:59.307Z","createdAt":"2022-04-20T12:27:54.563Z","updatedAt":"2022-04-20T12:27:54.563Z"},"results":{"didActionComplete":false,"lastActionId":126149,"expired":true,"finished":true},"error":null,"startTime":"2022-04-20T12:27:54.628Z","endTime":"2022-04-20T12:28:06.050Z","createdAt":"2022-04-20T12:27:54.620Z","updatedAt":"2022-04-20T12:27:54.620Z"}},{"Entity":"172.30.xxx.xxx","EntityResult":{"id":418,"type":"responseAction","status":"COMPLETED","metadata":{"id":8,"type":"quarantine","status":"QUEUED","computerName":"EXLAB2019-xxx.xxx.xxx","userId":1,"userName":"tanium","options":{"packageName":"Apply Windows IPsec Quarantine","packageParameters":[{"key":"$1","value":null},{"key":"$2","value":null},{"key":"$3","value":null},{"key":"$4","value":null},{"key":"$5","value":null},{"key":"$6","value":null},{"key":"$7","value":null},{"key":"$8","value":null},{"key":"$9","value":null}],"packageSkipLockFlag":false},"results":{},"expirationTime":"1970-01-01T00:09:59.307Z","createdAt":"2022-04-20T12:28:09.706Z","updatedAt":"2022-04-20T12:28:09.706Z"},"results":{"didActionComplete":false,"lastActionId":126151,"expired":true,"finished":true},"error":null,"startTime":"2022-04-20T12:28:09.771Z","endTime":"2022-04-20T12:28:20.625Z","createdAt":"2022-04-20T12:28:09.762Z","updatedAt":"2022-04-20T12:28:09.762Z"}}]
```



#### List Endpoint Events
List events related to the endpoints from Tanium. Action works with Tanium Threat Response API. Supported Entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event Type|Specify the type of the event that needs to be returned.|False|List|Combined|
|Time Frame|Specify a time frame for the results. If "Alert Time Till Now" is selected, action will use start time of the alert as start time for the search and end time will be current time. If "30 Minutes Around Alert Time" is selected, action will search the alerts 30 minutes before the alert happened till the 30 minutes after the alert has happened.  Same idea applies to "1 Hour Around Alert Time" and "5 Minutes Around Alert Time". If "Custom" is selected, you also need to provide "Start Time".|False|List|Last Hour|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Sort Field|Specify what parameter should be used for sorting.|False|String|timestamp|
|Sort Order|Specify the order of sorting.|False|List|ASC|
|Max Events To Return|Specify how many events to return per entity. Default: 50. Maximum: 500.|False|String|50|



##### JSON Results
```json
[{"Entity":"172.30.xxx.xxx","EntityResult":[{"create_time":"2022-01-18 11:59:52.000","end_time":null,"exit_code":null,"pid":2,"process_path":"kthreadd","id":"720575xxxxxxxx","process_table_id":"720575xxxxxxxx","parent_process_table_id":"720575xxxxxxxxx","parent_pid":-1,"user_name":"root","group_name":"root","hash_type_name":null,"hash":null,"process_command_line":null,"parent_path":"<Unknown Process>","parent_command_line":"<Unknown Process>","parent_hash":null,"create_time_raw":1642507192000,"end_time_raw":null}]},{"Entity":"centos-xxxx","EntityResult":[{"id":"461168xxxxxxxxxxxxx","timestamp":"2022-04-04 15:04:30.293","timestamp_raw":1649084670293,"pid":865,"process_table_id":"72057xxxxxxxxxxx","process_path":"/opt/SumoCollector/jre/bin/java","file":"/opt/SumoCollector/config/blades/000000000AB1F252.json.new.25","operation":"Create","event_operation_id":0,"user_name":"root","group_name":"root","details":null}]}]
```



#### Enrich Entities
Enrich entities using information from Tanium. Supported entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Additional Fields|Specify additional fields to fetch from Tanium for entity enrichment. Parameter accepts multiple values as a comma separated string.|False|String||



##### JSON Results
```json
[{"Entity":"machine_name","EntityResult":{"Computer ID":"3864xxxxx","Operating System":"CentOS Linux release 7.9.2009 (Core)","OS Platform":"Linux","Service Pack":"N/A on Linux","Domain Name":"(none)","Uptime":"21 days","System UUID":"422284D8-BBAA-63FC-xxxx-xxxxx","IP Address":"172.30.xx.xx, 172.xx.xx.1, fe80::be5d:xxx:xxx:xxx","Computer Name":"machine_name","Username":"No User"}}]
```



#### Get Task Details
Retrieve details about a task in Tanium. Action works with Tanium Threat Response API. Note: Action is running as async, if "Wait For Completion" is enabled, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task IDs|Specify a comma-separated list of task ids for which you want to fetch details.|True|String||
|Wait For Completion|If enabled, action will wait for the task to have status "Completed", "Incomplete", "Error".|False|Boolean|true|



##### JSON Results
```json
[{"id":125,"type":"deployIntel","status":"COMPLETED","metadata":{"serviceId":"7111f160-935d-xxxxxxxxxxxx","revision":71,"intelMapping":[{"profileId":1,"sourceLabelMapping":[{"sourceId":5}],"generateDefenderAlerts":true,"generateDeepInstinctAlerts":false},{"profileId":2,"sourceLabelMapping":[{"sourceId":5}],"generateDefenderAlerts":true,"generateDeepInstinctAlerts":false},{"profileId":3,"sourceLabelMapping":[{"sourceId":5}],"generateDefenderAlerts":true,"generateDeepInstinctAlerts":false}]},"results":{"id":491,"name":"Threat Response - Intel Cache"},"error":null,"startTime":"2022-04-05T12:51:20.800Z","endTime":"2022-04-05T12:52:03.367Z","createdAt":"2022-04-05T12:51:20.792Z","updatedAt":"2022-04-05T12:51:20.792Z"}]
```



#### Create Question
Create a new Tanium question based on the specified parameters, and the question is immediately asked. Action returns question id that can be passed to “Get Question Results” action to get question results. Note that the action is not working with Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Question Text|Specify the contents of Tanium question. Example: Get Operating System from all machines|True|String||



##### JSON Results
```json
{"data":{"id":481524545454}}
```



#### Create Connection
Create connection to the endpoint in Tanium. Supported Entities: Hostname, IP Address.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity":"centos-xxxx","EntityResult":"remote:centos-xxx:xxxxxxxx:"}]
```



#### Download File
Download a file from endpoints in Tanium. Action works with Tanium Threat Response API. Supported Entities: Hostname, IP Address. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|Specify the absolute path of the files on the endpoint that needs to be downloaded.|True|String||
|Download Folder Path|Specify the path to the folder, where you want to store the files.|True|String||
|Overwrite|If enabled, action will overwrite the file with the same name.|False|Boolean|false|



##### JSON Results
```json
{"absolute_file_path":["file_path_1","file_path_2"],"entity":[{"identifier":"","task_details":{"id":81,"type":"fileDownload","status":"COMPLETED","metadata":{"connection":"remote:centos-xxxxxxxxxx","paths":["/tmp/saaj-impl.jar"],"compress":"true"},"results":{"completed":["/tmp/saaj-impl.jar"],"failed":[],"fileResults":[{"response":{"source":"/tmp/saaj-impl.jar","target":"/opt/Tanium/TaniumModuleServer/services/threat-response-service/tmp/4965e791-db87-xxxxxxxxxx","totalBytes":503502,"transferHash":"5402c16c3873a722b9xxxxxxxxxxxxxxxx","totalTimeMs":260,"avgBytesPerSecond":504123.0769230769},"uuid":"eb5077b3-9b02-xxxxxxxxxxxxxx","finalPath":"/opt/Tanium/TaniumModuleServer/services/threat-response-files/evidence/files/eb5077b3-9b02-xxxxxxxxxxxx.zip"}]},"error":null,"startTime":"2022-03-01T14:38:23.952Z","endTime":"2022-03-01T14:38:24.559Z","createdAt":"2022-03-01T14:38:23.943Z","updatedAt":"2022-03-01T14:38:23.943Z"}}]}
```



#### Get Question Results
Fetch results for the Tanium question. Action is a Siemplify async action. Note that the action is not working with Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Question ID|Specify Tanium question id to get results for.|True|String||
|Create Case Wall Table|If enabled, action will create a case wall table as part of action results.|False|Boolean|true|
|Max Rows to Return|Specify the max number of rows action should return for the question.|True|String|50|



##### JSON Results
```json
{"id": 1, "report_count": 3, "saved_question_id": 0, "question_id": 1, "seconds_since_issued": 600, "issue_seconds": 0, "expire_seconds": 600, "tested": 3, "passed": 3, "mr_tested": 3, "mr_passed": 3, "estimated_total": 3, "select_count": 3, "error_count": 0, "no_results_count": 0, "row_count": 3, "row_count_machines": 3, "item_count": 3, "filtered_row_count": 3, "filtered_row_count_machines": 3, "columns": [{"hash": 1, "name": "IP Address", "type": 5}, {"hash": 2, "name": "Computer Name", "type": 1}, {"hash": 3, "name": "Operating System", "type": 1}], "rows": [{"IP Address": ["fe80::1ff:fe23:4567:890a", "172.16.0.23"], "Computer Name": ["workstation-001"], "Operating System": ["Windows Server 2022 Datacenter"]}, {"IP Address": ["fe80::1ff:fe23:4567:890b"], "Computer Name": ["workstation-002"], "Operating System": ["Windows Server 2019 Standard Evaluation"]}, {"IP Address": ["10.30.0.21"], "Computer Name": ["linux-server-prod.internal"], "Operating System": ["Debian 12.12"]}]}
```









