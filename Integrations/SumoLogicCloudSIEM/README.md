
# SumoLogicCloudSIEM

Sumo Logic Cloud SIEM provides threat detection and incident response for modern IT environments such as hybrid, multi-cloud, and microservices. Whether you’re looking for your first cloud SIEM, replacing your legacy SIEM, looking for an add-on solution to monitor cloud workloads, or seeking to consolidate your SIEM tools, Sumo Logic is the leading solution in the market.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Sumo Logic Cloud SIEM instance.|True|String|https://{instance}|
|API Key|API Key of the Sumo Logic Cloud SIEM account. Note: API key has priority over other authentication method.|False|Password|*****|
|Access ID|Access ID of the Sumo Logic Cloud SIEM account. Note: both Access ID and Access Key are required for this type of authentication.|False|String||
|Access Key|Access Key of the Sumo Logic Cloud SIEM account. Note: both Access ID and Access Key are required for this type of authentication.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Sumo Logic Cloud SIEM server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|bs4-0.0.2-py2.py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|soupsieve-2.8.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|python_dateutil-2.8.2-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Add Tags To Insight
Add tags to insight in Sumo Logic Cloud SIEM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|Specify the ID of the insight to which action needs to add tags.|True|String||
|Tags|Specify a comma-separated list of tags that needs to be added in insight.|True|String||



##### JSON Results
```json
{"data": {"artifacts": [], "assignedTo": "tip.labops", "assignee": {"displayName": "tip.labops@siemplify.co", "username": "tip.labops"}, "closed": "2022-03-11T08:48:56.310452", "closedBy": "tip.labops", "confidence": 0.1, "created": "2022-03-11T08:48:26.030204", "description": "Detects multiple failed login attempts from a single source with unique usernames over a 24 hour timeframe. This is designed to catch both slow and quick password spray type attacks. The threshold and time frame can be adjusted based on the customer's environment.", "entity": {"entityType": "_ip", "hostname": null, "id": "_ip-172.xx.xx.xx", "macAddress": null, "name": "172.xx.xx.xx", "sensorZone": "", "value": "172.xx.xx.xx"}, "id": "dbc30c20-xxxxxxxxxxxxxxxxx", "lastUpdated": "2022-03-16T11:46:08.415597", "lastUpdatedBy": null, "name": "Initial Access", "orgId": "siemplify", "readableId": "INSIGHT-13xxxx", "resolution": null, "severity": "CRITICAL", "signals": [{"allRecords": [{"action": "failed password attempt", "bro_dns_answers": [], "bro_file_bytes": {}, "bro_file_connUids": [], "bro_flow_service": [], "bro_ftp_pendingCommands": [], "bro_http_cookieVars": [], "bro_http_origFuids": [], "bro_http_origMimeTypes": [], "bro_http_request_headers": {}, "bro_http_request_proxied": [], "bro_http_response_headers": {}, "bro_http_response_respFuids": [], "bro_http_response_respMimeTypes": [], "bro_http_tags": [], "bro_http_uriVars": [], "bro_kerberos_clientCert": {}, "bro_kerberos_serverCert": {}, "bro_sip_headers": {}, "bro_sip_requestPath": [], "bro_sip_responsePath": [], "bro_ssl_certChainFuids": [], "bro_ssl_clientCertChainFuids": [], "cseSignal": {}, "day": 11, "device_ip": "172.xx.xx.xx", "device_ip_ipv4IntValue": 280000000, "device_ip_isInternal": true, "device_ip_version": 4, "fieldTags": {}, "fields": {"auth_method": "ssh2", "endpoint_ip": "172.xx.xx.xx", "endpoint_username": "1ewk0XJn", "event_message": "Failed password for invalid user", "src_port": "59088"}, "friendlyName": "record", "hour": 8, "http_requestHeaders": {}, "listMatches": [], "matchedItems": [], "metadata_deviceEventId": "citrix_xenserver_auth_message", "metadata_mapperName": "Citrix Xenserver Auth Message", "metadata_mapperUid": "bcc62402-xxxxxxxxxxxxx", "metadata_parseTime": 1646987453926, "metadata_product": "Hypervisor", "metadata_productGuid": "6751ee25-xxxxxxxxxxxxxx", "metadata_receiptTime": 1646987443, "metadata_relayHostname": "centos-002", "metadata_schemaVersion": 3, "metadata_sensorId": "0b52e838-xxxxxxxxxxxxxx", "metadata_sensorInformation": {}, "metadata_sensorZone": "default", "metadata_vendor": "Citrix", "month": 3, "normalizedAction": "logon", "objectType": "Authentication", "srcDevice_ip": "172.xx.xx.xx", "srcDevice_ip_ipv4IntValue": 280000000, "srcDevice_ip_isInternal": true, "srcDevice_ip_version": 4, "success": false, "timestamp": 1646987443000, "uid": "c2e6188b-xxxxxxxxxxxxx", "user_username": "1ewk0XJn", "user_username_raw": "1ewk0XJn", "year": 2022}], "artifacts": [], "contentType": "ANOMALY", "description": "Detects multiple failed login attempts from a single source with unique usernames over a 24 hour timeframe. This is designed to catch both slow and quick password spray type attacks. The threshold and time frame can be adjusted based on the customer's environment.", "id": "b4adb0dc-xxxxxxxxxxxxx", "name": "Password Attack", "recordCount": 10, "recordTypes": [], "ruleId": "THRESHOLD-S00xxx", "severity": 4, "stage": "Initial Access", "tags": ["_mitreAttackTactic:TA0001", "_mitreAttackTactic:TA0006", "_mitreAttackTechnique:T1110", "_mitreAttackTechnique:T1078", "_mitreAttackTechnique:T1078.001", "_mitreAttackTechnique:T1078.002", "_mitreAttackTechnique:T1078.003", "_mitreAttackTechnique:T1078.004", "_mitreAttackTechnique:T1586", "_mitreAttackTechnique:T1586.001", "_mitreAttackTechnique:T1586.002", "_mitreAttackTactic:TA0008", "_mitreAttackTechnique:T1110.003", "_mitreAttackTechnique:T1110.002", "_mitreAttackTechnique:T1110.001"], "timestamp": "2022-03-11T08:31:28"}], "source": "USER", "status": {"displayName": "In Progress", "name": "inprogress"}, "subResolution": null, "tags": ["In Progress", "_mitreAttackTactic:TA0001", "_mitreAttackTactic:TA0006", "_mitreAttackTactic:TA0008", "_mitreAttackTechnique:T1078", "_mitreAttackTechnique:T1078.001", "_mitreAttackTechnique:T1078.002", "_mitreAttackTechnique:T1078.003", "_mitreAttackTechnique:T1078.004", "_mitreAttackTechnique:T1110", "_mitreAttackTechnique:T1110.001", "_mitreAttackTechnique:T1110.002", "_mitreAttackTechnique:T1110.003", "_mitreAttackTechnique:T1586", "_mitreAttackTechnique:T1586.001", "_mitreAttackTechnique:T1586.002", "\u0561\u057d\u0564\u0561\u057d"], "teamAssignedTo": null, "timeToDetection": 1271.030204, "timeToRemediation": 30.280248, "timeToResponse": 21.186055, "timestamp": "2022-03-11T08:31:28"}, "errors": []}
```



#### Enrich Entities
Enrich entities using information from Sumo Logic Cloud SIEM. Supported entities: Hostname, User, IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight containing all of the retrieved information about the entity.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "172.30.xxx.xxx", "EntityResult": {"activityScore": 8, "criticality": "severity / 7", "entityType": "_ip", "firstSeen": null, "hostname": null, "id": "_ip-172.30.xxx.xxx", "inventory": [], "isSuppressed": false, "isWhitelisted": false, "lastSeen": "2022-03-11T09:44:53", "macAddress": null, "name": "172.30.xxx.xxx", "sensorZone": null, "tags": [], "value": "172.30.xxx.xxx"}}, {"Entity": "defaultaccount", "EntityResult": {"activityScore": 0, "criticality": null, "entityType": "_username", "firstSeen": null, "hostname": null, "id": "_username-defaultaccount", "inventory": [{"department": null, "emails": [], "givenName": null, "groups": [], "lastName": null, "metadata": {"accountExpires": "92233720325598xxxxx", "cn": "DefaultAccount", "distinguishedName": "CN=DefaultAccount,CN=Users,DC=exlab,DC=local", "lastLogon": 0, "objectCategory": "CN=Person,CN=Schema,CN=Configuration,DC=exlab,DC=local", "objectClass": "top;person;organizationalPerson;user", "objectGUID": "{914a0d9a-xxxx-4dd7-b992-d6xxxxxxxxxx}", "objectSid": "S-1-5-21-34797xxxxx-4256118348-xxxxxxxxxx-xxx", "primaryGroupId": "5xx", "pwdLastSet": 0, "sAMAccountName": "DefaultAccount", "userAccountControl": "66xxx", "whenCreated": "3/17/2022 2:59:39 PM"}, "middleName": null, "normalizedUsername": "defaultaccount", "parsedTime": "2022-03-24 14:56:38.546000", "source": "Active Directory", "timestamp": "2022-03-24 14:56:38.546000", "uniqueId": "S-1-5-21-34797xxxxx-4256118348-xxxxxxxxxx-xxx", "username": "DefaultAccount"}], "isSuppressed": false, "isWhitelisted": false, "lastSeen": null, "macAddress": null, "name": "defaultaccount", "sensorZone": null, "tags": [], "value": "defaultaccount"}}, {"Entity": "ex16-xxxx.exlab", "EntityResult": {"activityScore": 0, "criticality": "Test2", "entityType": "_hostname", "firstSeen": null, "hostname": "ex16-xxxx.exlab", "id": "_hostname-ex16--xxxx.exlab", "inventory": [{"computerName": "EX16-xxxx", "groups": [], "hostname": "ex16-xxxx.exlab.local", "ip": [], "location": null, "mac": null, "metadata": {"accountExpires": "92233720325598xxxxx", "cn": "EX16-xxxx", "dNSHostName": "ex16-xxxx.exlab.local", "distinguishedName": "CN=EX16-xxxx,OU=Domain Controllers,DC=exlab,DC=local", "lastLogon": "13292605xxxxxxxxxx", "objectCategory": "CN=Computer,CN=Schema,CN=Configuration,DC=exlab,DC=local", "objectClass": "top;person;organizationalPerson;user;computer", "objectGUID": "{a9d03316-bda8-xxxx-bea7-05xxxxxxxxxx}", "objectSid": "S-1-5-21-34797xxxxx-4256118348-xxxxxxxxxx-xxxx", "operatingSystem": "Windows Server 2016 Standard Evaluation", "operatingSystemVersion": "10.0 (14393)", "primaryGroupId": "5xx", "pwdLastSet": "13292002xxxxxxxxxx", "sAMAccountName": "EX16-xxxx$", "userAccountControl": "532xxx", "whenCreated": "3/17/2022 3:00:58 PM"}, "natIp": [], "normalizedComputerName": null, "normalizedHostname": "ex16-xxxx.exlab", "os": "Windows Server 2016 Standard Evaluation", "osVersion": "10.0 (14393)", "parsedTime": "2022-03-24 14:56:38.802000", "source": "Active Directory", "timestamp": "2022-03-24 14:56:38.802000", "uniqueId": "{a9d03316-bda8-xxxx-bea7-05xxxxxxxxxx}"}], "isSuppressed": false, "isWhitelisted": false, "lastSeen": null, "macAddress": null, "name": "ex16-xxxx.exlab", "sensorZone": null, "tags": [], "value": "ex16-xxxx.exlab"}}]
```



#### Update Insight
Update insight status in Sumo Logic Cloud SIEM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|Specify the ID of the insight needs to be updated.|True|String||
|Status|Specify what status to set for the insight.|True|List|Select One|
|Assignee Type|Specify the assignee type for the "Assignee" parameter.|True|List|User|
|Assignee|Specify the assignee identifier.|False|String||



##### JSON Results
```json
{"data": {"artifacts": [], "assignedTo": null, "assignee": null, "closed": null, "closedBy": null, "confidence": 0.25, "created": "2022-03-28T09:31:19.593192", "description": "Detects multiple failed login attempts for the same username over a 1 hour timeframe. This is designed to catch attacks leveraging domain resources to attempt credential validation. The threshold and time frame can be adjusted based on the customer's environment.", "entity": {"entityType": "_username", "hostname": null, "id": "_username-administrator", "macAddress": null, "name": "administrator", "sensorZone": "", "value": "administrator"}, "id": "2fe4e9f8-xxxx-4849-8a9f-1fxxxxxxxxxx", "lastUpdated": "2022-04-04T10:16:13.397311", "lastUpdatedBy": null, "name": "Initial Access", "orgId": "test", "readableId": "INSIGHT-13xxx", "recordSummaryFields": [], "resolution": null, "severity": "LOW", "source": "USER", "status": {"displayName": "New", "name": "new"}, "subResolution": null, "tags": ["_mitreAttackTactic:TA0xxx", "_mitreAttackTactic:TA0xxx"], "teamAssignedTo": null, "timeToDetection": 290.810192, "timeToRemediation": null, "timeToResponse": 607493.8023, "timestamp": "2022-03-28T09:27:11.557000"}, "errors": []}
```



#### Search Entity Signals
Search signals related to entities in Sumo Logic Cloud SIEM. Supported entities: IP Address, Hostname, Username.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Lowest Severity To Return|Specify the lowest severity number that will be used to return signals. Maximum: 10.|False|String|5|
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time". If "30 Minutes Around Alert Time" is selected, action will search the alerts 30 minutes before the alert happened till the 30 minutes after the alert has happened.  Same idea applies to "1 Hour Around Alert Time" and "5 Minutes Around Alert Time".|False|List|Last Hour|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Max Signals To Return|Specify how many signals to return per entity. Default: 50.|False|String|50|



##### JSON Results
```json
[{"Entity": "172.30.xxx.xx", "EntityResult": [{"allRecords": [{"action": "failed password attempt", "bro_dns_answers": [], "bro_file_bytes": {}, "bro_file_connUids": [], "bro_flow_service": [], "bro_ftp_pendingCommands": [], "bro_http_cookieVars": [], "bro_http_origFuids": [], "bro_http_origMimeTypes": [], "bro_http_request_headers": {}, "bro_http_request_proxied": [], "bro_http_response_headers": {}, "bro_http_response_respFuids": [], "bro_http_response_respMimeTypes": [], "bro_http_tags": [], "bro_http_uriVars": [], "bro_kerberos_clientCert": {}, "bro_kerberos_serverCert": {}, "bro_sip_headers": {}, "bro_sip_requestPath": [], "bro_sip_responsePath": [], "bro_ssl_certChainFuids": [], "bro_ssl_clientCertChainFuids": [], "cseSignal": {}, "day": 11, "device_ip": "172.30.xxx.xx", "device_ip_ipv4IntValue": 288000000, "device_ip_isInternal": true, "device_ip_version": 4, "fieldTags": {}, "fields": {"auth_method": "ssh2", "endpoint_ip": "172.30.xxx.xx", "endpoint_username": "bL0xxxx", "event_message": "Failed password for invalid user", "src_port": "39788"}, "friendlyName": "record", "hour": 10, "http_requestHeaders": {}, "listMatches": [], "matchedItems": [], "metadata_deviceEventId": "citrix_xenserver_auth_message", "metadata_mapperName": "Citrix Xenserver Auth Message", "metadata_mapperUid": "bcc62402-2870-xxxxx", "metadata_parseTime": 1646994593976, "metadata_product": "Hypervisor", "metadata_productGuid": "6751ee25-xxxxxxx", "metadata_receiptTime": 1646994592, "metadata_relayHostname": "centos-002", "metadata_schemaVersion": 3, "metadata_sensorId": "0b52e838-2dbd-xxxxxx", "metadata_sensorInformation": {}, "metadata_sensorZone": "default", "metadata_vendor": "Citrix", "month": 3, "normalizedAction": "logon", "objectType": "Authentication", "srcDevice_ip": "172.30.xxx.xx", "srcDevice_ip_ipv4IntValue": 288000000, "srcDevice_ip_isInternal": true, "srcDevice_ip_version": 4, "success": false, "timestamp": 1646994592000, "uid": "7a89ebd4-xxxxxxxx", "user_username": "bL0xxxx", "user_username_raw": "bL0xxxx", "year": 2022}], "artifacts": [], "contentType": "ANOMALY", "description": "Detects multiple failed login attempts from a single source with unique usernames over a 24 hour timeframe. This is designed to catch both slow and quick password spray type attacks. The threshold and time frame can be adjusted based on the customer's environment.", "entity": {"entityType": "_ip", "hostname": null, "id": "_ip-172.30.xxx.xx", "macAddress": null, "name": "172.30.xxx.xx", "sensorZone": "", "value": "172.30.xxx.xx"}, "id": "a9288779-xxxxxxxxx", "name": "Password Attack", "recordCount": 10, "recordTypes": [], "ruleId": "THRESHOLD-S00xxxx", "severity": 4, "stage": "Initial Access", "suppressed": true, "tags": ["_mitreAttackTactic:TA0001", "_mitreAttackTactic:TA0006", "_mitreAttackTechnique:T1110", "_mitreAttackTechnique:T1078", "_mitreAttackTechnique:T1078.001", "_mitreAttackTechnique:T1078.002", "_mitreAttackTechnique:T1078.003", "_mitreAttackTechnique:T1078.004", "_mitreAttackTechnique:T1586", "_mitreAttackTechnique:T1586.001", "_mitreAttackTechnique:T1586.002", "_mitreAttackTactic:TA0008", "_mitreAttackTechnique:T1110.003", "_mitreAttackTechnique:T1110.002", "_mitreAttackTechnique:T1110.001"], "timestamp": "2022-03-11T10:29:52"}, {"allRecords": [{"action": "failed password attempt", "bro_dns_answers": [], "bro_file_bytes": {}, "bro_file_connUids": [], "bro_flow_service": [], "bro_ftp_pendingCommands": [], "bro_http_cookieVars": [], "bro_http_origFuids": [], "bro_http_origMimeTypes": [], "bro_http_request_headers": {}, "bro_http_request_proxied": [], "bro_http_response_headers": {}, "bro_http_response_respFuids": [], "bro_http_response_respMimeTypes": [], "bro_http_tags": [], "bro_http_uriVars": [], "bro_kerberos_clientCert": {}, "bro_kerberos_serverCert": {}, "bro_sip_headers": {}, "bro_sip_requestPath": [], "bro_sip_responsePath": [], "bro_ssl_certChainFuids": [], "bro_ssl_clientCertChainFuids": [], "cseSignal": {}, "day": 11, "device_ip": "172.30.xxx.xx", "device_ip_ipv4IntValue": 288000000, "device_ip_isInternal": true, "device_ip_version": 4, "fieldTags": {}, "fields": {"auth_method": "ssh2", "endpoint_ip": "172.30.xxx.xx", "endpoint_username": "letmein", "event_message": "Failed password for invalid user", "src_port": "36376"}, "friendlyName": "record", "hour": 9, "http_requestHeaders": {}, "listMatches": [], "matchedItems": [], "metadata_deviceEventId": "citrix_xenserver_auth_message", "metadata_mapperName": "Citrix Xenserver Auth Message", "metadata_mapperUid": "bcc62402-xxxxxxxxx", "metadata_parseTime": 1646991849187, "metadata_product": "Hypervisor", "metadata_productGuid": "6751ee25-xxxxxxxx", "metadata_receiptTime": 1646991845, "metadata_relayHostname": "centos-002", "metadata_schemaVersion": 3, "metadata_sensorId": "0b52e838-xxxxxxxxx", "metadata_sensorInformation": {}, "metadata_sensorZone": "default", "metadata_vendor": "Citrix", "month": 3, "normalizedAction": "logon", "objectType": "Authentication", "srcDevice_ip": "172.30.xxx.xx", "srcDevice_ip_ipv4IntValue": 288000000, "srcDevice_ip_isInternal": true, "srcDevice_ip_version": 4, "success": false, "timestamp": 1646991845000, "uid": "f4bca20a-xxxxxxxx", "user_username": "letmein", "user_username_raw": "letmein", "year": 2022}], "artifacts": [], "contentType": "ANOMALY", "description": "Detects multiple failed login attempts for the same username over a 24 hour timeframe. This is designed to catch both slow and quick brute force type attacks. The threshold and time frame can be adjusted based on the customer's environment.", "entity": {"entityType": "_ip", "hostname": null, "id": "_ip-172.30.xxx.xx", "macAddress": null, "name": "172.30.xxx.xx", "sensorZone": "", "value": "172.30.xxx.xx"}, "id": "8e6a7bd1-xxxxxxxx", "name": "Brute Force Attempt", "recordCount": 10, "recordTypes": [], "ruleId": "THRESHOLD-S00xxxx", "severity": 4, "stage": "Initial Access", "suppressed": true, "tags": ["_mitreAttackTactic:TA0001", "_mitreAttackTactic:TA0006", "_mitreAttackTechnique:T1110", "_mitreAttackTechnique:T1078", "_mitreAttackTechnique:T1586", "_mitreAttackTactic:TA0008", "_mitreAttackTechnique:T1110.002", "_mitreAttackTechnique:T1110.001"], "timestamp": "2022-03-11T09:44:53"}]}, {"Entity": "scaner", "EntityResult": [{"allRecords": [{"action": "User logon to account disabled by administrator", "application": "NtLmSsp ", "bro_dns_answers": [], "bro_file_bytes": {}, "bro_file_connUids": [], "bro_flow_service": [], "bro_ftp_pendingCommands": [], "bro_http_cookieVars": [], "bro_http_origFuids": [], "bro_http_origMimeTypes": [], "bro_http_request_headers": {}, "bro_http_request_proxied": [], "bro_http_response_headers": {}, "bro_http_response_respFuids": [], "bro_http_response_respMimeTypes": [], "bro_http_tags": [], "bro_http_uriVars": [], "bro_kerberos_clientCert": {}, "bro_kerberos_serverCert": {}, "bro_sip_headers": {}, "bro_sip_requestPath": [], "bro_sip_responsePath": [], "bro_ssl_certChainFuids": [], "bro_ssl_clientCertChainFuids": [], "cseSignal": {}, "day": 22, "description": "An account failed to log on", "device_hostname": "wh01-sumologic", "device_hostname_raw": "WH01-SUMOLogic", "dstDevice_hostname": "wh01-sumologic", "dstDevice_hostname_raw": "WH01-SUMOLogic", "errorCode": "0xc0000072", "errorText": "User logon to account disabled by administrator", "fieldTags": {}, "fields": {"Channel": "Security", "Computer": "WH01-SUMOLogic", "Correlation.ActivityID": "{cb654074-xxxxxxxx}", "EventData.AuthenticationPackageName": "NTLM", "EventData.FailureReason": "%%2310", "EventData.IpAddress": "172.30.xxx.xx", "EventData.IpPort": "52894", "EventData.KeyLength": "0", "EventData.LogonProcessName": "NtLmSsp ", "EventData.LogonType": "3", "EventData.ProcessId": "0x0", "EventData.Status": "0xc000006e", "EventData.SubStatus": "0xc0000072", "EventData.SubjectLogonId": "0x0", "EventData.SubjectUserSid": "S-1-0-0", "EventData.TargetUserName": "administrator", "EventData.TargetUserSid": "S-1-0-0", "EventData.WorkstationName": "scaner", "EventID": "xxx", "EventRecordID": "xxx", "Execution.ProcessID": "xxx", "Execution.ThreadID": "xxx", "Keywords": "Audit Failure", "Level": "Information", "Opcode": "Info", "Provider.Guid": "{54849625-xxxxxxxxx}", "Provider.Name": "Microsoft-Windows-Security-Auditing", "Task": "xxxx", "TimeCreated": "2022-03-22T10:03:19.8483526Z", "TimeCreated.SystemTime": "2022-03-22T10:03:19.8483526Z", "Version": "0"}, "friendlyName": "record", "hour": 10, "http_requestHeaders": {}, "listMatches": [], "logonType": "Network", "matchedItems": [], "metadata_deviceEventId": "Security-xxxx", "metadata_mapperName": "Windows - Security - xxxx", "metadata_mapperUid": "0e3b7ced-xxxxxx", "metadata_orgId": "0000000000xxxx", "metadata_parseTime": 1647943457131, "metadata_product": "Windows", "metadata_productGuid": "1ff7546c-xxxxxxx", "metadata_receiptTime": 1647943423, "metadata_schemaVersion": 3, "metadata_sensorId": "0000000000xxxx", "metadata_sensorInformation": {}, "metadata_sensorZone": "default", "metadata_sourceCategory": "cse/windows/event", "metadata_sourceMessageId": "117619xxxxxx", "metadata_vendor": "Microsoft", "month": 3, "normalizedAction": "domainLogon", "objectType": "Authentication", "srcDevice_hostname": "scaner", "srcDevice_hostname_raw": "scaner", "srcDevice_ip": "172.30.xxx.xx", "srcDevice_ip_ipv4IntValue": 288000000, "srcDevice_ip_isInternal": true, "srcDevice_ip_version": 4, "success": false, "timestamp": 1647943399848, "uid": "9c56970e-xxxxxxx", "user_authDomain": "", "user_username": "administrator", "user_username_raw": "administrator", "year": 2022}], "artifacts": [], "contentType": "RULE", "description": "Detects a disabled account being used for a logon attempt in a Windows environment.", "entity": {"entityType": "_hostname", "hostname": "scaner", "id": "_hostname-scaner", "macAddress": null, "name": "scaner", "sensorZone": "", "value": "scaner"}, "id": "364abd8c-xxxxxxxx", "name": "Disabled Account Logon Attempt", "recordCount": 1, "recordTypes": [], "ruleId": "LEGACY-xxxxx", "severity": 6, "stage": "Initial Access", "suppressed": true, "tags": ["_mitreAttackTactic:TA0001", "_mitreAttackTactic:TA0003", "_mitreAttackTactic:TA0004", "_mitreAttackTactic:TA0005", "_mitreAttackTactic:TA0006", "_mitreAttackTechnique:T1078", "_mitreAttackTechnique:T1078.001", "_mitreAttackTechnique:T1078.002", "_mitreAttackTechnique:T1078.003", "_mitreAttackTechnique:T1110", "_mitreAttackTechnique:T1110.001", "_mitreAttackTechnique:T1110.002", "_mitreAttackTechnique:T1110.003", "_mitreAttackTechnique:T1110.004"], "timestamp": "2022-03-22T10:03:19.848000"}]}, {"Entity": "administrator", "EntityResult": [{"allRecords": [{"action": "User logon to account disabled by administrator", "application": "NtLmSsp ", "bro_dns_answers": [], "bro_file_bytes": {}, "bro_file_connUids": [], "bro_flow_service": [], "bro_ftp_pendingCommands": [], "bro_http_cookieVars": [], "bro_http_origFuids": [], "bro_http_origMimeTypes": [], "bro_http_request_headers": {}, "bro_http_request_proxied": [], "bro_http_response_headers": {}, "bro_http_response_respFuids": [], "bro_http_response_respMimeTypes": [], "bro_http_tags": [], "bro_http_uriVars": [], "bro_kerberos_clientCert": {}, "bro_kerberos_serverCert": {}, "bro_sip_headers": {}, "bro_sip_requestPath": [], "bro_sip_responsePath": [], "bro_ssl_certChainFuids": [], "bro_ssl_clientCertChainFuids": [], "cseSignal": {}, "day": 22, "description": "An account failed to log on", "device_hostname": "wh01-sumologic", "device_hostname_raw": "WH01-SUMOLogic", "dstDevice_hostname": "wh01-sumologic", "dstDevice_hostname_raw": "WH01-SUMOLogic", "errorCode": "0xc0000072", "errorText": "User logon to account disabled by administrator", "fieldTags": {}, "fields": {"Channel": "Security", "Computer": "WH01-SUMOLogic", "Correlation.ActivityID": "{cb654074-xxxxxxxx}", "EventData.AuthenticationPackageName": "NTLM", "EventData.FailureReason": "%%2310", "EventData.IpAddress": "172.30.xxx.xx", "EventData.IpPort": "57878", "EventData.KeyLength": "0", "EventData.LogonProcessName": "NtLmSsp ", "EventData.LogonType": "3", "EventData.ProcessId": "0x0", "EventData.Status": "0xc000006e", "EventData.SubStatus": "0xc0000072", "EventData.SubjectLogonId": "0x0", "EventData.SubjectUserSid": "S-1-0-0", "EventData.TargetUserName": "administrator", "EventData.TargetUserSid": "S-1-0-0", "EventID": "xxx", "EventRecordID": "xxxx", "Execution.ProcessID": "xxx", "Execution.ThreadID": "xxx", "Keywords": "Audit Failure", "Level": "Information", "Opcode": "Info", "Provider.Guid": "{54849625-xxxxxxxx}", "Provider.Name": "Microsoft-Windows-Security-Auditing", "Task": "xxxx", "TimeCreated": "2022-03-22T10:36:13.0029699Z", "TimeCreated.SystemTime": "2022-03-22T10:36:13.0029699Z", "Version": "0"}, "friendlyName": "record", "hour": 10, "http_requestHeaders": {}, "listMatches": [], "logonType": "Network", "matchedItems": [], "metadata_deviceEventId": "Security-xxx", "metadata_mapperName": "Windows - Security - xxx", "metadata_mapperUid": "0e3b7ced-xxxxxxx", "metadata_orgId": "0000000000xxxx", "metadata_parseTime": 1647945488956, "metadata_product": "Windows", "metadata_productGuid": "1ff7546c-xxxxxxxx", "metadata_receiptTime": 1647945399, "metadata_schemaVersion": 3, "metadata_sensorId": "0000000000xxxx", "metadata_sensorInformation": {}, "metadata_sensorZone": "default", "metadata_sourceCategory": "cse/windows/event", "metadata_sourceMessageId": "1176xxxxxxxxx", "metadata_vendor": "Microsoft", "month": 3, "normalizedAction": "domainLogon", "objectType": "Authentication", "srcDevice_ip": "172.30.xxx.xx", "srcDevice_ip_ipv4IntValue": 288000000, "srcDevice_ip_isInternal": true, "srcDevice_ip_version": 4, "success": false, "timestamp": 1647945373002, "uid": "45909162-xxxxxxx", "user_authDomain": "", "user_username": "administrator", "user_username_raw": "administrator", "year": 2022}], "artifacts": [], "contentType": "RULE", "description": "Detects a disabled account being used for a logon attempt in a Windows environment.", "entity": {"entityType": "_username", "hostname": null, "id": "_username-administrator", "macAddress": null, "name": "administrator", "sensorZone": "", "value": "administrator"}, "id": "a8fc77a5-xxxxxxxxx", "name": "Disabled Account Logon Attempt", "recordCount": 1, "recordTypes": [], "ruleId": "LEGACY-xxxx", "severity": 6, "stage": "Initial Access", "suppressed": true, "tags": ["_mitreAttackTactic:TA0001", "_mitreAttackTactic:TA0003", "_mitreAttackTactic:TA0004", "_mitreAttackTactic:TA0005", "_mitreAttackTactic:TA0006", "_mitreAttackTechnique:T1078", "_mitreAttackTechnique:T1078.001", "_mitreAttackTechnique:T1078.002", "_mitreAttackTechnique:T1078.003", "_mitreAttackTechnique:T1110", "_mitreAttackTechnique:T1110.001", "_mitreAttackTechnique:T1110.002", "_mitreAttackTechnique:T1110.003", "_mitreAttackTechnique:T1110.004"], "timestamp": "2022-03-22T10:36:13.002000"}]}]
```



#### Add Comment To Insight
Add a comment to insight in Sumo Logic Cloud SIEM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|Specify the ID of the insight to which action needs to add a comment.|True|String||
|Comment|Specify the comment that needs to be added in insight.|True|String||



##### JSON Results
```json
{"data": {"author": {"username": "tip.labops"}, "body": "In Progress", "id": "1", "timestamp": "2022-03-16T12:03:56.472109"}, "errors": []}
```



#### Ping
Test connectivity to the Sumo Logic Cloud SIEM with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Sumo Logic Cloud SIEM - Insights Connector
Pull information about insights from Sumo Logic Cloud SIEM. Note: dynamic list filter works with "name" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|generalized_data_name|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of the Sumo Logic Cloud SIEM instance.|True|String|https://{instance}|
|API Key|API Key of the Sumo Logic Cloud SIEM account. Note: API key has priority over other authentication method.|False|Password|*****|
|Access ID|Access ID of the Sumo Logic Cloud SIEM account. Note: both Access ID and Access Key are required for this type of authentication.|False|String||
|Access Key|Access Key of the Sumo Logic Cloud SIEM account. Note: both Access ID and Access Key are required for this type of authentication.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Sumo Logic Cloud SIEM server is valid.|False|Boolean|true|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch insights. Possible values: Low, Medium, High, Critical. If nothing is specified, the connector will ingest insights with all severities.|False|String||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve insights from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Insights To Fetch|How many insights to process per one connector iteration. Default: 20.|False|Integer|20|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




