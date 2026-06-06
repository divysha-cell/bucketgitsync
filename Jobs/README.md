## 12 Actions Monitor
Notifies of all the actions, that have individually failed at least 3 times, in the last 3 hours


**Run Interval In Seconds:** 3600



Readme Addon## CA Close Ticket In CA For Closed Case - AutoTest 1
Automated test job instance. Index: 21


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_d3d5c93b|
|Password|String|True|test_str_8dc5c72e|
|Group Filter|String||test_str_71a9ace1|
|Group Field|String|True|test_str_2fc60d4d|
|Ticket Final Status|String|True|test_str_4d58cb23|
|Script Name|String|True|test_str_0aa2c6bb|


Readme Addon## CA Close Ticket In CA For Closed Case - AutoTest 2
Automated test job instance. Index: 48


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_7f96754e|
|Password|String|True|test_str_8e10676d|
|Group Filter|String||test_str_7d62316e|
|Group Field|String|True|test_str_3373b772|
|Ticket Final Status|String|True|test_str_11501259|
|Script Name|String|True|test_str_b32ca1d9|


Readme Addon## CA Close Ticket In CA For Closed Case
Sync closure of the tickets at the CA Desk Manager with Siemplify cases closure.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|http://x.x.x.x:<port>|
|Username|String|True|dfghj|
|Password|String|True|dfgvhbn|
|Group Filter|String||Test|
|Group Field|String|True|group.combo_name|
|Ticket Final Status|String|True|Closed|
|Script Name|String|True|TEST CLOSE|


Readme Addon## Case Federation Sync Job - AutoTest 1
Automated test job instance. Index: 26


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|True|test_str_ae9b9e4f|
|API Key|Password|True|*****|


Readme Addon## Case Federation Sync Job
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|True|hgfds|
|API Key|Password|True|*****|


Readme Addon## Case Federation Sync Job234567
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|True|ertyu|
|API Key|Password|True|*****|


Readme Addon## Case Federation Sync Job2345678
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|True|456789|
|API Key|Password|True|*****|


Readme Addon## Case Federation Sync Job4567890
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|True|hgfdsgf|
|API Key|Password|True|*****|


Readme Addon## Close Cases Based On Search - AutoTest 1
Automated test job instance. Index: 3


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Search Payload|String||test_str_2f6fd6f0|
|Close Comment|String|True|test_str_06350e2b|
|Close Reason|Integer|True|60|
|Root Cause|String|True|test_str_a77fb6dd|


Readme Addon## Close Cases Based On Search - AutoTest 2
Automated test job instance. Index: 30


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Search Payload|String||test_str_a9b580bb|
|Close Comment|String|True|test_str_1058bec6|
|Close Reason|Integer|True|60|
|Root Cause|String|True|test_str_8aa8d771|


Readme Addon## Close Cases Based On Search
This job will close all cases based on a search query.  The Search Payload is the payload used in the 'CaseSearchEverything' API call.  To get an example of this value, go to Search in the UI and open Developer Tools.  Search for the cases to delete.  Look for the "CaseSearchEverything" api call in DevTools.  Copy the JSON payload of the POST request and paste in "Search Payload".  The Close Reason should be 0 or 1.   0 = malicious 1  = not malicious.  Root Cause comes from Settings -> Case Data -> Case Close Root Cause


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Search Payload|String||{}|
|Close Comment|String|True|Closed|
|Close Reason|Integer|True|1|
|Root Cause|String|True|Malicious|


Readme Addon## Google Chronicle Alerts Creator Job - AutoTest 1
Automated test job instance. Index: 17


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://backstory.googleapis.com|
|Verify SSL|Boolean||true|
|User's Service Account|Password||*****|
|Workload Identity Email|Password||*****|


Readme Addon## Google Chronicle Alerts Creator Job - AutoTest 2
Automated test job instance. Index: 44


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://backstory.googleapis.com|
|Verify SSL|Boolean||true|
|User's Service Account|Password||*****|
|Workload Identity Email|Password||*****|


Readme Addon## Google Chronicle Sync Job - AutoTest 1
Automated test job instance. Index: 16


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String||test_str_8a5a8e7f|
|Verify SSL|Boolean||true|
|User's Service Account|Password||*****|
|Workload Identity Email|Password||*****|


Readme Addon## Google Chronicle Sync Job - AutoTest 2
Automated test job instance. Index: 43


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String||test_str_2278967c|
|Verify SSL|Boolean||true|
|User's Service Account|Password||*****|
|Workload Identity Email|Password||*****|


Readme Addon## Oauth Token Expiry Notification Job - AutoTest 1
Automated test job instance. Index: 18


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Mail Server Address|String|True|test_str_d41e4630|
|Mail Address for sending notifications|String|True|test_str_1468f195|
|Notifications Recipients List|String|True|test_str_1d94b7be|
|Client ID|String|True|test_str_180170ff|
|Tenant (Directory) ID|String|True|test_str_0218d6e8|
|Client Secret|Password||*****|
|Refresh Token|Password|True|*****|


Readme Addon## Oauth Token Expiry Notification Job - AutoTest 2
Automated test job instance. Index: 45


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Mail Server Address|String|True|test_str_759d9441|
|Mail Address for sending notifications|String|True|test_str_719d6020|
|Notifications Recipients List|String|True|test_str_bbe6c65e|
|Client ID|String|True|test_str_e3f84569|
|Tenant (Directory) ID|String|True|test_str_77017193|
|Client Secret|Password||*****|
|Refresh Token|Password|True|*****|


Readme Addon## Oauth Token Expiry Notification Job
Note that the job is deprecated and will be removed in the next 6 months. Oauth Token Expiry Notification Job is recommended to use if integration is working with Oauth refresh tokens. Refresh tokens are valid only for 90 days, after that User will need to create a new refresh token to use in the integration. This job will send reminder emails to the configured recipient list when the token will expire in 10, 5 and 1 day. Once a new token is set in this job, the notification timer will start over.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Mail Server Address|String|True|outlook.office365.com|
|Mail Address for sending notifications|String|True|gfd|
|Notifications Recipients List|String|True|gfds|
|Client ID|String|True|hgfdsa|
|Tenant (Directory) ID|String|True|ds|
|Client Secret|Password||*****|
|Refresh Token|Password|True|*****|


Readme Addon## Refresh Token Renewal Job - AutoTest 1
Automated test job instance. Index: 11


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String||test_str_16b9e576|


Readme Addon## Refresh Token Renewal Job - AutoTest 2
Automated test job instance. Index: 38


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String||test_str_01b6a432|


Readme Addon## Refresh Token Renewal Job
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 82800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|||


Readme Addon## Refresh Token Renewal Job1234556789
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 82800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|||


Readme Addon## Refresh Token Renewal Job2345678
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|||
|Connector Names|String|||


Readme Addon## Refresh Token Renewal Job23456789
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 86400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String||rewf|
|Connector Names|String||ds|


Readme Addon## Refresh Token Renewal Job23466543
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Connector Names|String|||
|Integration Environments|String|||


Readme Addon## Refresh Token Renewal Job34
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String||Default|
|Connector Names|String||test|


Readme Addon## Refresh Token Renewal Job345678
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 79200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|||
|Connector Names|String|||


Readme Addon## Sync Alerts - AutoTest 1
Automated test job instance. Index: 9


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_fe5fd756|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Integer||60|
|Verify SSL|Boolean||true|
|API Token|Password|True|*****|


Readme Addon## Sync Alerts - AutoTest 2
Automated test job instance. Index: 36


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_1704429d|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Integer||60|
|API Token|Password|True|*****|
|Verify SSL|Boolean||true|


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
|Max Hours Backwards|Integer|True|24|
|Sync Assignee|Boolean||true|
|Verify SSL|Boolean||false|
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
|Max Hours Backwards|Integer||24|
|Verify SSL|Boolean||true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Alerts234567
This job will synchronize Google SecOps Alerts and SentinelOne alerts. The job synchronizes status. Requires “SentinelOne Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” you will need to add an “Alert_ID” Alert Context Value for the job to be able to find the correct information.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|sdfghj|
|Max Hours Backwards|Integer||24|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer|True|24|
|Sync Assignee|Boolean||false|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer|True|24|
|Sync Assignee|Boolean||false|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer||24|
|Verify SSL|Boolean||true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Closed Incidents - AutoTest 1
Automated test job instance. Index: 5


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_04c12ccb|
|Verify SSL|Boolean||true|
|Client ID|String||test_str_a48f3bc3|
|Use Oauth Authentication|Boolean||true|
|Max Hours Backwards|Integer||60|
|Table Name|String|True|test_str_bd7da694|
|Client Secret|Password||*****|
|Refresh Token|Password||*****|
|Password|Password|True|*****|


Readme Addon## Sync Closed Incidents - AutoTest 2
Automated test job instance. Index: 32


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_f7f0b372|
|Verify SSL|Boolean||true|
|Client ID|String||test_str_0583a459|
|Use Oauth Authentication|Boolean||true|
|Max Hours Backwards|Integer||60|
|Table Name|String|True|test_str_9697e225|
|Password|Password|True|*****|
|Client Secret|Password||*****|
|Refresh Token|Password||*****|


Readme Addon## Sync Closed Incidents By Tag - AutoTest 1
Automated test job instance. Index: 23


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Incident Table|String|True|test_str_e4b23bef|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_19468cde|
|Environment|String||Default Environment|
|Max Hours Backwards|String||test_str_5b2b5f9a|
|Verify SSL|Boolean||true|
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
|Environment|String|||
|Max Hours Backwards|String||24|
|Verify SSL|Boolean||true|
|Password|Password|True|*****|


Readme Addon## Sync Closed Incidents
This job will synchronize closed ServiceNow incidents and Google SecOps alerts. This job works with ServiceNow incidents that were ingested as alerts and also cases, which contains tag “ServiceNow” and “TICKET_ID” context value with Incident Number inside of it.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|True|dfghj|
|Verify SSL|Boolean||true|
|Client ID|String||fghjk|
|Use Oauth Authentication|Boolean||false|
|Max Hours Backwards|Integer||24|
|Table Name|String|True|test|
|Password|Password|True|*****|
|Client Secret|Password||*****|
|Refresh Token|Password||*****|


Readme Addon## Sync Closed Requests By Tag - AutoTest 1
Automated test job instance. Index: 1


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String||test_str_a2298248|
|Verify SSL|Boolean||true|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag - AutoTest 2
Automated test job instance. Index: 28


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Key|Password|True|*****|
|Api Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String||test_str_7abbd683|
|Verify SSL|Boolean||true|


Readme Addon## Sync Closed Requests By Tag
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Key|Password|True|*****|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String||24|
|Verify SSL|Boolean||true|


Readme Addon## Sync Closed Requests By Tag34567
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 82800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Key|Password|True|*****|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String||24|
|Verify SSL|Boolean||true|


Readme Addon## Sync Closed Requests By Tag345678
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String||24|
|Verify SSL|Boolean||true|
|Api Key|Password|True|*****|


Readme Addon## Sync Closed Requests By Tag56789
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Key|Password|True|*****|
|Api Root|String|True|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String||24|
|Verify SSL|Boolean||true|


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
|Ticket Type Field|Boolean||true|
|Analyst Type Field|Boolean||true|
|Time Stamp Field|Boolean||true|
|Timezone String|Boolean||true|
|Password|Password|True|*****|


Readme Addon## Sync Comments - AutoTest 2
Automated test job instance. Index: 49


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Timezone String|Boolean||true|
|Password|Password|True|*****|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_9991e669|
|Summery Field|String|True|test_str_23338201|
|Ticket Fields|String|True|test_str_bff826e4|
|Script Name|String|True|test_str_99b37f79|
|Ticket Type Field|Boolean||true|
|Analyst Type Field|Boolean||true|
|Time Stamp Field|Boolean||true|


Readme Addon## Sync Comments56
Sync comments from CA Desk Manager to Siemplify.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|http://x.x.x.x:<port>|
|Username|String|True|dfgh|
|Summery Field|String|True|summery.combo_name|
|Password|Password|True|*****|
|Ticket Fields|String|True|summery.combo_name,customer.combo_name,category.sym,status.sym,priority.sym,active,log_agent.combo_name,assignee.combo_name,group.combo_name,affected_service.name,severity.sym,urgency.sym,impact.sym,problem.ref_num,resolution_code.sym,call_back_date,change.chg_ref_num,caused_by_chg.chg_ref_num,external_system_ticket,resolution_method.sym,symptom_code.sym,requested_by.combo_name,persistent_id,summary,description,open_date,last_mod_dt,resolve_date,close_date,ref_num|
|Script Name|String|True|Test|
|Ticket Type Field|Boolean||true|
|Analyst Type Field|Boolean||true|
|Time Stamp Field|Boolean||true|
|Timezone String|Boolean||true|


Readme Addon## Sync IOC Feeds - AutoTest 1
Automated test job instance. Index: 0


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|test_str_1a8c222d|
|Max IOCs Per Feed|Integer||60|
|Reference List Prefix|String||test_str_1769bf33|
|API Root|String|True|https://backstory.googleapis.com|
|Company ID|String|True|test_str_65d1afee|
|Verify SSL|Boolean||true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds - AutoTest 2
Automated test job instance. Index: 27


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|test_str_b513d705|
|Max IOCs Per Feed|Integer||60|
|Reference List Prefix|String||test_str_8402e1d5|
|API Root|String|True|https://backstory.googleapis.com|
|Company ID|String|True|test_str_647cb01f|
|Verify SSL|Boolean||true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|hgfds|
|Max IOCs Per Feed|Integer||5000|
|Reference List Prefix|String||SOCRadar_IOC|
|API Root|String|True|https://platform.socradar.com/api|
|Company ID|String|True|gfds|
|Verify SSL|Boolean||true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds109
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** 25200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|ertfyguhi|
|Max IOCs Per Feed|Integer||5000|
|Reference List Prefix|String||SOCRadar_IOC|
|API Root|String|True|https://platform.socradar.com/api|
|Company ID|String|True|erftgyhujk|
|Verify SSL|Boolean||true|
|API Key|Password|True|*****|


Readme Addon## Sync IOC Feeds345678
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|True|gfds|
|Max IOCs Per Feed|Integer||5000|
|Reference List Prefix|String||SOCRadar_IOC|
|API Root|String|True|https://platform.socradar.com/api|
|Company ID|String|True|jhgfdsgfds|
|Verify SSL|Boolean||true|
|API Key|Password|True|*****|


Readme Addon## Sync Incidents - AutoTest 1
Automated test job instance. Index: 10


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_db77b1df|
|Api Root|String||https://backstory.googleapis.com|
|Api Key ID|String|True|test_str_45b5455b|
|Max Hours Backwards|Integer|True|60|
|User Mapping JSON|String||test_str_c955c4f7|
|Verify SSL|Boolean||true|
|Api Key|Password|True|*****|


Readme Addon## Sync Incidents - AutoTest 2
Automated test job instance. Index: 37


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Key ID|String|True|test_str_7195bc49|
|Max Hours Backwards|Integer|True|60|
|User Mapping JSON|String||test_str_2300834b|
|Verify SSL|Boolean||true|
|Environment Name|String|True|test_str_67910e8f|
|Api Root|String||https://backstory.googleapis.com|
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
|Max Hours Backwards|Integer|True|60|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer|True|60|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer|True|24|
|Verify SSL|Boolean||false|
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
|Max Hours Backwards|Integer||60|
|Sync Assignee|Boolean||true|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer||60|
|Sync Assignee|Boolean||true|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer||24|
|Sync Assignee|Boolean||true|
|Verify SSL|Boolean||true|
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
|Max Hours Backwards|Integer||24|
|Verify SSL|Boolean||true|
|Client Secret|Password|True|*****|


Readme Addon## Sync Incidents234
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Api Root|String||jhgf|
|Api Key ID|String|True|gfds|
|Max Hours Backwards|Integer|True|24|
|User Mapping JSON|String||{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean||true|
|Api Key|Password|True|*****|


Readme Addon## Sync Incidents34567
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Key|Password|True|*****|
|Environment Name|String|True|Default Environment|
|Api Root|String||sdfghj|
|Api Key ID|String|True|dfghj|
|Max Hours Backwards|Integer|True|24|
|User Mapping JSON|String||{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean||true|


Readme Addon## Sync Incidents5778
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 2678400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Api Root|String||dfghj|
|Api Key ID|String|True|sdfghjk|
|Max Hours Backwards|Integer|True|24|
|User Mapping JSON|String||{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean||true|
|Api Key|Password|True|*****|


Readme Addon## Sync Table Record Comments - AutoTest 1
Automated test job instance. Index: 6


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_1ac16942|
|Verify SSL|Boolean||true|
|Client ID|String||test_str_5937d6d4|
|Use Oauth Authentication|Boolean||true|
|Table Name|String|True|test_str_844ef772|
|Password|Password|True|*****|
|Client Secret|Password||*****|
|Refresh Token|Password||*****|


Readme Addon## Sync Table Record Comments - AutoTest 2
Automated test job instance. Index: 33


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_5be7dcd0|
|Verify SSL|Boolean||true|
|Client ID|String||test_str_1056b44c|
|Use Oauth Authentication|Boolean||true|
|Table Name|String|True|test_str_b97c562c|
|Password|Password|True|*****|
|Client Secret|Password||*****|
|Refresh Token|Password||*****|


Readme Addon## Sync Table Record Comments By Tag - AutoTest 1
Automated test job instance. Index: 7


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://backstory.googleapis.com|
|Username|String|True|test_str_b5c62078|
|Table Name|String|True|test_str_285db0e1|
|Verify SSL|Boolean||true|
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
|Verify SSL|Boolean||true|
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
|Verify SSL|Boolean||true|
|Password|Password|True|*****|


Readme Addon## Sync Threats - AutoTest 1
Automated test job instance. Index: 8


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_bcbbbb82|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Integer|True|60|
|Verify SSL|Boolean||true|
|API Token|Password|True|*****|


Readme Addon## Sync Threats - AutoTest 2
Automated test job instance. Index: 35


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|test_str_7413932e|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|Integer|True|60|
|Verify SSL|Boolean||true|
|API Token|Password|True|*****|


Readme Addon## Sync Threats 2
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|hgfds|
|Max Hours Backwards|Integer|True|24|
|Verify SSL|Boolean||false|
|API Token|Password|True|*****|


Readme Addon## Sync Threats
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|dfghj|
|Max Hours Backwards|Integer|True|24|
|Verify SSL|Boolean||true|
|API Token|Password|True|*****|


Readme Addon## Sync Threats345678
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|API Root|String|True|dfghjk|
|Max Hours Backwards|Integer|True|24|
|Verify SSL|Boolean||true|
|API Token|Password|True|*****|


Readme Addon## Tag Untouched Cases - AutoTest 1
Automated test job instance. Index: 2


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|test_str_0e8e9989|
|Unmodified Time|Integer|True|60|


Readme Addon## Tag Untouched Cases - AutoTest 2
Automated test job instance. Index: 29


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|test_str_59ac47ef|
|Unmodified Time|Integer|True|60|


Readme Addon## Tag Untouched Cases new
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 2699940

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Reviewfghm|
|Unmodified Time|Integer|True|8|


Readme Addon## Tag Untouched Cases
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Review|
|Unmodified Time|Integer|True|8|


Readme Addon## Tag Untouched Cases34567
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Reertyuview|
|Unmodified Time|Integer|True|8e|


Readme Addon## Tag Untouched Cases7890
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** 18000

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|True|Open Case Review|
|Unmodified Time|Integer|True|8|


Readme Addon## Token Renewal Job - AutoTest 1
Automated test job instance. Index: 19


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String||test_str_69f41f92|
|Connector Names|String||test_str_d0fc2dea|


Readme Addon## Token Renewal Job - AutoTest 2
Automated test job instance. Index: 46


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String||test_str_7cc8d114|
|Connector Names|String||test_str_484a35ff|


Readme Addon