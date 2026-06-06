## Refresh Token Renewal Job1234556789
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 82800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||


Readme Addon## Refresh Token Renewal Job2345678
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||
|Connector Names|String|False||


Readme Addon## Refresh Token Renewal Job23456789
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 86400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False|rewf|
|Connector Names|String|False|ds|


Readme Addon## Refresh Token Renewal Job23466543
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||
|Connector Names|String|False||


Readme Addon## Refresh Token Renewal Job34
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False|Default|
|Connector Names|String|False|test|


Readme Addon## Refresh Token Renewal Job345678
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 79200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||
|Connector Names|String|False||


Readme Addon## Sync Alerts - AutoTest 1
Automated test job instance. Index: 9


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_fe5fd756|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Int|False|60|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Sync Alerts - AutoTest 2
Automated test job instance. Index: 36


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_1704429d|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Int|False|60|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Sync Alerts
This job synchronizes Google SecOps Alerts and Microsoft Defender XDR Alerts. It ensures that comments and status are synchronized bi-directionally between both systems. Note: Assignee synchronization occurs exclusively from Microsoft Defender to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the "Microsoft Defender XDR Alert" tag. If the alert didn’t originate from "Microsoft 365 Defender - Incidents Connector",  you will need to add an "Alert_ID" context value to the alert for the job to be able to find the correct information.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Login API Root|String|True|https://login.microsoftonline.com|
|Graph API Root|String|True|https://graph.microsoft.com|
|API Root|String|True|https://api.security.microsoft.com|
|Tenant ID|String|True|dfghj|
|Client ID|String|True|dfghjkl|
|Max Hours Backwards|Int|True|24|
|Sync Assignee|Boolean|False|true|
|Verify SSL|Boolean|False|false|
|Client Secret|Password|True|*****|


Readme Addon## Sync Alerts2
This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.


**Run Interval In Seconds:** 360240

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|https://api.crowdstrike.com|
|Client ID|String|True|dfghj|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Alerts234567
This job will synchronize Google SecOps Alerts and SentinelOne alerts. The job synchronizes status. Requires “SentinelOne Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” you will need to add an “Alert_ID” Alert Context Value for the job to be able to find the correct information.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|sdfghj|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Sync Alerts2345678
This job synchronizes Google SecOps Alerts and Microsoft Defender XDR Alerts. It ensures that comments and status are synchronized bi-directionally between both systems. Note: Assignee synchronization occurs exclusively from Microsoft Defender to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the "Microsoft Defender XDR Alert" tag. If the alert didn’t originate from "Microsoft 365 Defender - Incidents Connector",  you will need to add an "Alert_ID" context value to the alert for the job to be able to find the correct information.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Login API Root|String|True|https://login.microsoftonline.com|
|Graph API Root|String|True|https://graph.microsoft.com|
|API Root|String|True|https://api.security.microsoft.com|
|Tenant ID|String|True|fds|
|Client ID|String|True|gfd|
|Max Hours Backwards|Int|True|24|
|Sync Assignee|Boolean|False|false|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Alerts2345678765
This job synchronizes Google SecOps Alerts and Microsoft Defender XDR Alerts. It ensures that comments and status are synchronized bi-directionally between both systems. Note: Assignee synchronization occurs exclusively from Microsoft Defender to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the "Microsoft Defender XDR Alert" tag. If the alert didn’t originate from "Microsoft 365 Defender - Incidents Connector",  you will need to add an "Alert_ID" context value to the alert for the job to be able to find the correct information.


**Run Interval In Seconds:** 18000

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Login API Root|String|True|https://login.microsoftonline.com|
|Graph API Root|String|True|https://graph.microsoft.com|
|API Root|String|True|https://api.security.microsoft.com|
|Tenant ID|String|True|dfghj|
|Client ID|String|True|dfghj|
|Max Hours Backwards|Int|True|24|
|Sync Assignee|Boolean|False|false|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Alerts34567
This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|https://api.crowdstrike.com|
|Client ID|String|True|fds|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Closed Incidents - AutoTest 1
Automated test job instance. Index: 5


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_04c12ccb|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|test_str_a48f3bc3|
|Use Oauth Authentication|Boolean|False|true|
|Max Hours Backwards|Int|False|60|
|Table Name|String|True|test_str_bd7da694|
|Password|Password|True|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme Addon## Sync Closed Incidents - AutoTest 2
Automated test job instance. Index: 32


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_f7f0b372|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|test_str_0583a459|
|Use Oauth Authentication|Boolean|False|true|
|Max Hours Backwards|Int|False|60|
|Table Name|String|True|test_str_9697e225|
|Password|Password|True|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme Addon## Sync Closed Incidents By Tag - AutoTest 1
Automated test job instance. Index: 23


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Incident Table|String|True|test_str_e4b23bef|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_19468cde|
|Environment|String|False|Default Environment|
|Max Hours Backwards|String|False|test_str_5b2b5f9a|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Closed Incidents By Tag
This job will synchronize BMC Remedy ITSM incidents that were created within Siemplify Case playbook and Siemplify cases. Note: in BMC Remedy ITSM statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it's required for the case to have 2 tags. First tag should be "BMC Remedy ITSM" and the second should be with the prefix "BMC Remedy ITSM:{Incident ID}". Job can only close incidents that are assigned in BMC Remedy ITSM.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Incident Table|String|True|HPD:IncidentInterface|
|API Root|String|True|https://{IP}:{port}|
|Username|String|True|dfghj|
|Environment|String|False||
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Closed Incidents
This job will synchronize closed ServiceNow incidents and Google SecOps alerts. This job works with ServiceNow incidents that were ingested as alerts and also cases, which contains tag “ServiceNow” and “TICKET_ID” context value with Incident Number inside of it.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|True|dfghj|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|fghjk|
|Use Oauth Authentication|Boolean|False|false|
|Max Hours Backwards|Int|False|24|
|Table Name|String|True|test|
|Password|Password|True|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme Addon## Sync Closed Requests By Tag - AutoTest 1
Automated test job instance. Index: 1


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String|False|test_str_a2298248|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag - AutoTest 2
Automated test job instance. Index: 28


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String|False|test_str_7abbd683|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|whttp://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|false|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag34567
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 82800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag345678
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag56789
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Comments - AutoTest 1
Automated test job instance. Index: 22


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_bc9938ab|
|Summery Field|String|True|test_str_8c815b56|
|Ticket Fields|String|True|test_str_995296c3|
|Script Name|String|True|test_str_6868e232|
|Ticket Type Field|Boolean|False|true|
|Analyst Type Field|Boolean|False|true|
|Time Stamp Field|Boolean|False|true|
|Timezone String|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Comments - AutoTest 2
Automated test job instance. Index: 49


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_9991e669|
|Summery Field|String|True|test_str_23338201|
|Ticket Fields|String|True|test_str_bff826e4|
|Script Name|String|True|test_str_99b37f79|
|Ticket Type Field|Boolean|False|true|
|Analyst Type Field|Boolean|False|true|
|Time Stamp Field|Boolean|False|true|
|Timezone String|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Comments56
Sync comments from CA Desk Manager to Siemplify.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|http://x.x.x.x:<port>|
|Username|String|True|dfgh|
|Summery Field|String|True|summery.combo_name|
|Ticket Fields|String|True|summery.combo_name,customer.combo_name,category.sym,status.sym,priority.sym,active,log_agent.combo_name,assignee.combo_name,group.combo_name,affected_service.name,severity.sym,urgency.sym,impact.sym,problem.ref_num,resolution_code.sym,call_back_date,change.chg_ref_num,caused_by_chg.chg_ref_num,external_system_ticket,resolution_method.sym,symptom_code.sym,requested_by.combo_name,persistent_id,summary,description,open_date,last_mod_dt,resolve_date,close_date,ref_num|
|Script Name|String|True|Test|
|Ticket Type Field|Boolean|False|true|
|Analyst Type Field|Boolean|False|true|
|Time Stamp Field|Boolean|False|true|
|Timezone String|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync IOC Feeds - AutoTest 1
Automated test job instance. Index: 0


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|test_str_1a8c222d|
|Max IOCs Per Feed|Int|False|60|
|Reference List Prefix|String|False|test_str_1769bf33|
|API Root|String|True|https://backstory.googleapis.com|
|Company ID|String|True|test_str_65d1afee|
|Verify SSL|Boolean|False|true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds - AutoTest 2
Automated test job instance. Index: 27


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|test_str_b513d705|
|Max IOCs Per Feed|Int|False|60|
|Reference List Prefix|String|False|test_str_8402e1d5|
|API Root|String|True|https://backstory.googleapis.com|
|Company ID|String|True|test_str_647cb01f|
|Verify SSL|Boolean|False|true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|hgfds|
|Max IOCs Per Feed|Int|False|5000|
|Reference List Prefix|String|False|SOCRadar_IOC|
|API Root|String|True|https://platform.socradar.com/api|
|Company ID|String|True|gfds|
|Verify SSL|Boolean|False|true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds109
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** 25200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|ertfyguhi|
|Max IOCs Per Feed|Int|False|5000|
|Reference List Prefix|String|False|SOCRadar_IOC|
|API Root|String|True|https://platform.socradar.com/api|
|Company ID|String|True|erftgyhujk|
|Verify SSL|Boolean|False|true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds345678
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|gfds|
|Max IOCs Per Feed|Int|False|5000|
|Reference List Prefix|String|False|SOCRadar_IOC|
|API Root|String|True|https://platform.socradar.com/api|
|Company ID|String|True|jhgfdsgfds|
|Verify SSL|Boolean|False|true|
|API Key|Password|True|*****|


Readme Addon## Sync Incidents - AutoTest 1
Automated test job instance. Index: 10


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_db77b1df|
|Api Root|String|False|https://backstory.googleapis.com|
|Api Key ID|String|True|test_str_45b5455b|
|Max Hours Backwards|Int|True|60|
|User Mapping JSON|String|False|test_str_c955c4f7|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Incidents - AutoTest 2
Automated test job instance. Index: 37


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_67910e8f|
|Api Root|String|False|https://backstory.googleapis.com|
|Api Key ID|String|True|test_str_7195bc49|
|Max Hours Backwards|Int|True|60|
|User Mapping JSON|String|False|test_str_2300834b|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Incidents Job - AutoTest 1
Automated test job instance. Index: 4


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_db580b75|
|Sync Level|String|True|test_str_4b90fb73|
|Max Hours Backwards|Int|True|60|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Incidents Job - AutoTest 2
Automated test job instance. Index: 31


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_e18bb996|
|Sync Level|String|True|test_str_0270aa16|
|Max Hours Backwards|Int|True|60|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Incidents Job
This job will synchronize incidents fields and attachments that are related to case/alerts in ServiceNow. For the job to work, you need to have the "ServiceNow Incident Sync" tag added to the case and "TICKET_ID" context value added to either Case or Alert depending on the parameter "Sync Level". Example of the "TICKET_ID": "INC0000050,INC0000051".


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|True|wwss|
|Sync Level|String|True|Case|
|Max Hours Backwards|Int|True|24|
|Verify SSL|Boolean|False|false|
|Password|Password|True|*****|


Readme Addon## Sync Incidents V2 - AutoTest 1
Automated test job instance. Index: 14


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_908fed32|
|Azure Subscription ID|String|True|test_str_e5ea8e3a|
|Azure Active Directory ID|String|True|test_str_c5add7ce|
|OAUTH2 Login Endpoint Url|String|True|test_str_cb7fd90b|
|Management API Root|String|True|test_str_caf21def|
|Azure Resource Group|String|True|test_str_11a89f56|
|Azure Sentinel Workspace Name|String|True|test_str_c1e5a86f|
|Client ID|String|True|test_str_16f9d9b2|
|Max Hours Backwards|Int|False|60|
|Sync Assignee|Boolean|False|true|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Incidents V2 - AutoTest 2
Automated test job instance. Index: 41


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_9516b793|
|Azure Subscription ID|String|True|test_str_60ad98c2|
|Azure Active Directory ID|String|True|test_str_aa68a197|
|OAUTH2 Login Endpoint Url|String|True|test_str_a5153b1e|
|Management API Root|String|True|test_str_db0d4d9a|
|Azure Resource Group|String|True|test_str_93175e32|
|Azure Sentinel Workspace Name|String|True|test_str_eb338b99|
|Client ID|String|True|test_str_5b0d6b07|
|Max Hours Backwards|Int|False|60|
|Sync Assignee|Boolean|False|true|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Incidents V234567
Use the Sync Incidents V2 job to synchronize Google SecOps alerts with Microsoft Sentinel incidents. This job ensures that comments, statuses, and tags are synchronized bi-directionally between both systems. Note: Assignee and severity synchronization occurs exclusively from Microsoft Sentinel to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the Microsoft Sentinel Incident tag. This job only works on alerts from the Microsoft Azure Sentinel Incident Connector v2.


**Run Interval In Seconds:** 1987200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Azure Subscription ID|String|True|dfgh|
|Azure Active Directory ID|String|True|dfghj|
|OAUTH2 Login Endpoint Url|String|True|https://login.microsoftonline.com|
|Management API Root|String|True|https://management.azure.com|
|Azure Resource Group|String|True|cvbnm|
|Azure Sentinel Workspace Name|String|True|fghj|
|Client ID|String|True|dfghj|
|Max Hours Backwards|Int|False|24|
|Sync Assignee|Boolean|False|true|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Incidents
Deprecated. This job synchronizes Google SecOps Alerts and Microsoft Sentinel Incidents. It ensures that comments, status, and tags are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the “Microsoft Sentinel Incident” tag. If the alert didn’t originate from “Microsoft Azure Sentinel Incident Connector v2”,  you will need to add an “Incident_ID” context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 82800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Azure Active Directory ID|String|True|dfghj|
|OAUTH2 Login Endpoint Url|String|True|https://login.microsoftonline.com|
|API Root|String|True|https://graph.microsoft.com|
|Client ID|String|True|dfghjk,|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Incidents234
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Api Root|String|False|jhgf|
|Api Key ID|String|True|gfds|
|Max Hours Backwards|Int|True|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Incidents34567
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Api Root|String|False|sdfghj|
|Api Key ID|String|True|dfghj|
|Max Hours Backwards|Int|True|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Incidents5778
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 2678400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Api Root|String|False|dfghj|
|Api Key ID|String|True|sdfghjk|
|Max Hours Backwards|Int|True|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


Readme Addon## Sync Table Record Comments - AutoTest 1
Automated test job instance. Index: 6


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_1ac16942|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|test_str_5937d6d4|
|Use Oauth Authentication|Boolean|False|true|
|Table Name|String|True|test_str_844ef772|
|Password|Password|True|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme Addon## Sync Table Record Comments - AutoTest 2
Automated test job instance. Index: 33


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_5be7dcd0|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|test_str_1056b44c|
|Use Oauth Authentication|Boolean|False|true|
|Table Name|String|True|test_str_b97c562c|
|Password|Password|True|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme Addon## Sync Table Record Comments By Tag - AutoTest 1
Automated test job instance. Index: 7


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_b5c62078|
|Table Name|String|True|test_str_285db0e1|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Table Record Comments By Tag - AutoTest 2
Automated test job instance. Index: 34


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_8799174f|
|Table Name|String|True|test_str_7e3c04af|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Table Record Comments By Tag4567
This job will synchronize comments in ServiceNow table records and Siemplify cases. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceNow {table name}", for example, "ServiceNow incident" and the second should be with the prefix "ServiceNow TicketId: {TICKET_ID}". Example of the "TICKET_ID": "INC0000050,INC0000051".


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|True|gfds|
|Table Name|String|True|fds|
|Verify SSL|Boolean|False|true|
|Password|Password|True|*****|


Readme Addon## Sync Threats - AutoTest 1
Automated test job instance. Index: 8


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_bcbbbb82|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Int|True|60|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Sync Threats - AutoTest 2
Automated test job instance. Index: 35


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_7413932e|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Int|True|60|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Sync Threats 2
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|hgfds|
|Max Hours Backwards|Int|True|24|
|Verify SSL|Boolean|False|false|
|API Token|Password|True|*****|


Readme Addon## Sync Threats
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|dfghj|
|Max Hours Backwards|Int|True|24|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Sync Threats345678
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|dfghjk|
|Max Hours Backwards|Int|True|24|
|Verify SSL|Boolean|False|true|
|API Token|Password|True|*****|


Readme Addon## Tag Untouched Cases - AutoTest 1
Automated test job instance. Index: 2


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|test_str_0e8e9989|
|Unmodified Time|Int|True|60|


Readme Addon## Tag Untouched Cases - AutoTest 2
Automated test job instance. Index: 29


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|test_str_59ac47ef|
|Unmodified Time|Int|True|60|


Readme Addon## Tag Untouched Cases new
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 2699940

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Reviewfghm|
|Unmodified Time|Int|True|8|


Readme Addon## Tag Untouched Cases
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Review|
|Unmodified Time|Int|True|8|


Readme Addon## Tag Untouched Cases34567
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Reertyuview|
|Unmodified Time|Int|True|8e|


Readme Addon## Tag Untouched Cases7890
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 18000

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Review|
|Unmodified Time|Int|True|8|


Readme Addon## Token Renewal Job - AutoTest 1
Automated test job instance. Index: 19


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False|test_str_69f41f92|
|Connector Names|String|False|test_str_d0fc2dea|


Readme Addon## Token Renewal Job - AutoTest 2
Automated test job instance. Index: 46


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False|test_str_7cc8d114|
|Connector Names|String|False|test_str_484a35ff|


Readme Addon