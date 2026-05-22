# GitSync

## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Crowdstrike - Alerts Connector|Pull alerts from Crowdstrike. Dynamic List works with the "display_name" parameter. Note: To fetch identity protection detections use "Identity Protection Detections Connector".|False|
|n Crowdstrike - Alerts Connector|Pull alerts from Crowdstrike. Dynamic List works with the "display_name" parameter. Note: To fetch identity protection detections use "Identity Protection Detections Connector".|False|
|new Crowdstrike - Alerts Connector|Pull alerts from Crowdstrike. Dynamic List works with the "display_name" parameter. Note: To fetch identity protection detections use "Identity Protection Detections Connector".|False|
|Microsoft Graph Mail Delegated Connector|Connector can be used to fetch emails from the Microsoft Graph Mail service. Connector dynamic list can be used to filter specific values from the email body and subject parts using regexes. By default, regex is used to filter out the urls from the email. This connector uses Delegated Authentication in Microsoft 365 and requires interactive login of the user on behalf of which integration should communicate with Microsoft 365. To configure the connector, make sure that the integration configuration is already finished, and the refresh token needed to communicate with Office 365 is generated.|False|
|Palo Alto Cortex XDR Connector|Pull incidents from Palo Alto XDR. Dynamic List works with the “source” parameter.|False|


## Playbooks
|Name|Description|
|----|-----------|
|AWS EC2 Containment|This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.|
|AWS Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|AWS Instance Containment|This block allows you to stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.It uses a boolean input to control manual or automatic execution and returns the containment result, false on failure, or an empty value if no action is taken.|
|AWS User Containment|This block allows you to disable access for users referenced in the case, supporting containment actions during the incident response process. It uses a boolean input to control manual or automatic execution and returns the containment result, false on failure, or an empty value if no action is taken.|
|AWS Users Containment|An embedded workflow that can receive inputs and return an output.|
|Amazon Web Services Cloud Platform Starting Playbook|Amazon Web Services Cloud Platform Starting Playbook provides reference implementation of how Amazon Web Services Cloud Platform alerts can be processed in Google SecOps.|
|Azure User Containment|This block applies containment actions to Azure user accounts by resetting passwords or disabling accounts. A boolean input controls manual or automatic mode. In automatic mode, the Disable Account and Password Reset flags determine which actions run. It returns true if successful, false on failure, or empty if no action is taken.|
|GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|MITRE Enrichment|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|New Playbook||
|Nw Playbook||
|IMPORT 1 - SecMon_Enrichment_and_Triage_Block|An embedded workflow that can receive inputs and return an output.|
|SecMon_Enrichment_and_Triage_Block|An embedded workflow that can receive inputs and return an output.|
|Carbon Black Cloud Remediation||
|Copy of Carbon Black Cloud Remediation - 1||


## Visual Families
|Name|Description|
|----|-----------|
|AV_THBn|newaddedmanually|


## Jobs
|Name|Description|
|----|-----------|
|111Sync Comments - AutoTest 1|Automated test job instance configured by script. Index: 47|
|11Refresh Token Renewal Job - AutoTest 1|Automated test job instance configured by script. Index: 43|
|11Sync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 1|
|134Freshservice Sync Tickets Conversations Job - AutoTest 1|Automated test job instance configured by script. Index: 23|
|13Freshservice Sync Tickets Closure Job - AutoTest 1|Automated test job instance configured by script. Index: 24|
|1Case Federation Sync Job - AutoTest 1|Automated test job instance configured by script. Index: 0|
|1DRP Deduplication Job - AutoTest 1|Automated test job instance configured by script. Index: 20|
|1Fr2eshservice Sync Tickets Conversations Job - AutoTest 1|Automated test job instance configured by script. Index: 7|
|1Google Chronicle Alerts Creator Job - AutoTest 1|Automated test job instance configured by script. Index: 46|
|1Luminar IOC and Leaked Credentials Job - AutoTest 1|Automated test job instance configured by script. Index: 19|
|1Oauth Token Expiry Notification Job - AutoTest 1|Automated test job instance configured by script. Index: 22|
|1Sync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 2|
|2Case Federation Sync Job - AutoTest 1|Automated test job instance configured by script. Index: 0|
|2Sync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 2|
|2Token Renewal Job - AutoTest 1|Automated test job instance configured by script. Index: 21|
|2nSync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 1|
|3Case Federation Sync Job - AutoTest 1|Automated test job instance configured by script. Index: 0|
|3Sync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 2|
|4Case Federation Sync Job - AutoTest 1|Automated test job instance configured by script. Index: 0|
|4Sync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 2|
|5Case Federation Sync Job - AutoTest 1|Automated test job instance configured by script. Index: 0|
|5Sync Alerts|This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.|
|6Refresh Token Renewal Job|Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.|
|6new Sync Alerts|This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.|
|7Sync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 1|
|CA Close Ticket In CA For Closed Case - AutoTest 1|Automated test job instance configured by script. Index: 26|
|DRP Deduplication Job - AutoTest 1|Automated test job instance configured by script. Index: 4|
|Freshservice Sync Tickets Closure Job - AutoTest 11|Automated test job instance configured by script. Index: 8|
|Google Chronicle Sync Job - AutoTest 1|Automated test job instance configured by script. Index: 45|
|Google Chronicle Sync Job|This job will synchronize information about Chronicle SOAR Cases and Chronicle SOAR Alerts with Chronicle SIEM. Note: This job is only supported from Chronicle SOAR version 6.1.44 and higher.|
|LaunchScanAndGetAReport - AutoTest 1|Automated test job instance configured by script. Index: 31|
|Luminar IOC and Leaked Credentials Job - AutoTest 1|Automated test job instance configured by script. Index: 3|
|Oauth Token Expiry Notification Job - AutoTest 1|Automated test job instance configured by script. Index: 6|
|projects/project/locations/location/instances/instance/integrations/MicrosoftTeams/jobs/163/jobInstances/128|hey this is manually added Automated test job instance configured by script. Index: 52|
|S1ync Closed Alarms - AutoTest 1|Automated test job instance configured by script. Index: 27|
|S5ync Alerts - AutoTest 1|Automated test job instance configured by script. Index: 1|
|Sync Alarm Comments - AutoTest 1|Automated test job instance configured by script. Index: 29|
|Sync Case Comments - AutoTest 1|Automated test job instance configured by script. Index: 28|
|Sync Closed Alarms - AutoTest 1|Automated test job instance configured by script. Index: 9|
|Sync Closed Cases - AutoTest 1|Automated test job instance configured by script. Index: 30|
|Sync Closed Incidents By Tag - AutoTest 1|Automated test job instance configured by script. Index: 50|
|Sync Closure - AutoTest 1|Automated test job instance configured by script. Index: 48|
|Sync Comments - AutoTest 1|Automated test job instance configured by script. Index: 25|
|Sync Incidents V2 - AutoTest 1|Automated test job instance configured by script. Index: 32|
|Sync Incidents|This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.|
|Sync Security Incidents - AutoTest 1|Automated test job instance configured by script. Index: 44|
|Sync Table Record Comments - AutoTest 1|Automated test job instance configured by script. Index: 53|
|Sync Table Record Comments By Tag - AutoTest 1|Automated test job instance configured by script. Index: 54|
|SyncCloseOffenses - AutoTest 1|Automated test job instance configured by script. Index: 49|
|Token Renewal Job - AutoTest 1|Automated test job instance configured by script. Index: 5|

