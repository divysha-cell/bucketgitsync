# GitSync

## Integrations
|Name|Description|
|----|-----------|
|AWS Cloud Trail|AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting. In addition, you can use CloudTrail to detect unusual activity in your AWS accounts. These capabilities help simplify operational analysis and troubleshooting.|
|CA Service Desk Manager|CA Service Desk Manager is designed to help IT service desk analysts make every moment count through a dynamic experience so they can deliver great customer service without the fear of overbearing processes or metrics. With the solution, teams can embrace teamwork rather than working from siloed knowledge stashes and disjointed communications.|
|Google Chronicle|Google SecOps enables you to examine the aggregated security information for your enterprise going back for months or longer. Use Google SecOps to search across all of the domains accessed from within your enterprise. To enable the Google API client to communicate with the Backstory API you will need Google Developer Service Account Credential, https://developers.google.com/identity/protocols/OAuth2#serviceaccount.|
|Google SecOps AI Agents|This integration provides first-party AI agents for Google Chronicle. It allows users to leverage Google's advanced AI capabilities for security operations and threat intelligence within the Chronicle platform.|
|McAfee Mvision EDR V2|McAfee MVISION Endpoint Detection and Response (MVISION EDR) is a cloud-delivered service that enables you to detect advanced device threats, fully investigate, and quickly respond. Continuous data collection and advanced analytics detect suspicious behavior.|


## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|101 AWS Cloud Trail - Insights Connector|Pull insights from AWS Cloud Trail.|True|
|AWS Cloud Trail - Insights Connector|Pull insights from AWS Cloud Trail.|True|
|Connector_35_AWSCloudTrail|Pull insights from AWS Cloud Trail.|True|
|Connector_54_AmazonMacie|Pull findings from Amazon Macie. Note: Whitelist works with Finding types, for example, SensitiveData:S3Object/Personal.|True|
|Connector_23_AnomaliStaxx|Pull indicators from Anomali Staxx|False|
|Connector_19_Arcsight|Arcsight ESM Connector|False|
|Connector_31_AzureADIdentityProtection|Pull information about risk detections from Azure AD Identity Protection. Note: whitelist filter works with "riskEventType" parameter.|False|
|Connector_42_AzureSecurityCenter|Deprecation Notice! This connector is planned to be deprecated on 30th March 2027. Visit documentation for more information. Pull security alerts from Azure Security Center. Note: whitelist works with alertType field.|False|
|Connector_48_BMCHelixRemedyForce|Pull information about incidents from BMC Helix Remedyforce.|False|
|Connector_53_BlueLiv|Pull security threats from BlueLiv. Connector fetches all of the latest threats from BlueLiv modules. Whitelist and blacklist filters work with BlueLiv module types. For example, if you want to get threats only from Hacktivism modules, you can turn on the whitelist and type in the Hacktivism type name.|False|
|Connector_30_CiscoAMP|Pull security events from Cisco AMP into Siemplify. Note: whitelist works with eventType parameter.|False|
|Connector_44_Devo|Connector can be used to fetch alert records from Devo siem.logtrust.alert.info table. Connector whitelist can be used to ingest only specific types of alerts based on alert context value.|False|
|Connector_52_DigitalShadows|Connector ingest incidents from Digital Shadows into Siemplify.|False|
|Connector_45_EmailV2|Configured Connector_45_EmailV2|False|
|Connector_41_Extrahop|Pull information about detections from Extrahop. Note: whitelist filter works with "type" parameter.|False|
|Connector_46_FireEyeHelix|Pull alerts from FireEye Helix.|False|
|Connector_34_FireEyeNX|Connector ingests FireEye NX alert into Siemplify.|False|
|Connector_51_FortiAnalyzer|Pull information about alerts from FortiAnalyzer. Note: Dynamic list filter works with the "subject" parameter.|False|
|Connector_39_Fortigate|Pull information about different threat logs from Fortigate. Note: whitelist filter works with "eventtype" parameter.|False|
|Connector_37_FortinetFortiSIEM|Connector can be used to fetch FortiSIEM incidents. Connector whitelist can be used to ingest only specific types of incidents based on incident’s “eventType” attribute value. SourceGroupIdentifier of the connector can be used to group Siemplify alerts based on incident id.  Connector requires FortiSIEM version 6.3 or newer.|False|
|Connector_20_FreshworksFreshservice|Connector can be used to fetch Freshservice tickets to create Siemplify alerts from. Connector whitelist can be used to ingest only specific types of tickets - Incident or Service Request|False|
|Connector_28_Gmail|The Gmail Connector retrieves Gmail emails from the specified mailbox. To filter specific values from the email body and subject, use the dynamic list regular expressions in the following format: “key: regex”. For example, after finding a match for the following regex: “subject: (?<=Subject: ).*”, the connector creates a Google SecOps alert event and adds a new key with the “subject” name to it. The new key value matches the regular expression.|False|
|Connector_40_GoogleAlertCenter|Pull information about alerts from Google Alert Center. Note: whitelist filter works with "type" parameter.|False|
|Connector_1_GoogleChronicle|Pull information about Rule based alerts from Google Chronicle. Note: dynamic list is used for filtering purposes. For all of the details please visit the documentation portal.|True|
|Connector_25_GoogleThreatIntelligence|Use the Google Threat Intelligence - DTM Alerts Connector to retrieve alerts from Google Threat Intelligence. The dynamic listworks with the "alert_type" parameter.|False|
|Connector_33_HarmonyMobile|Pull information about alerts from Harmony Mobile. Note: whitelist filter works with "threat_factors" parameter.|False|
|Connector_43_IllusiveNetworks|Pull incidents with related forensic timeline from Illusive Networks. Note: This connector requires changes to the rate limiting on the Illusive Networks server. Default rate limit is too small. All of the steps are available in the documentation. Whitelisting and Blacklisting is done via type of the incident|False|
|Connector_27_Intsights|Configured Connector_27_Intsights|False|
|Connector_36_LogRhythm|Pull alerts from LogRhythm using Rest API. Note: this connector is only supported for LogRhythm version 7.7+.|False|
|Connector_21_McAfeeEPO|Pull events from the EPOEvents table into Siemplify. Whitelist works with Analyzer names.|False|
|Connector_55_McAfeeMvisionEPOV2|Pull events from McAfee Mvision EPO V2.|False|
|Connector_49_NozomiNetworks|Connector to fetch Nozomi Networks Alerts to Siemplify.|False|
|Connector_18_Office365CloudAppSecurity|Fetches alerts from Office 365 CloudApp Security.|False|
|Connector_26_OpenSearch|OpenSearch Connector|False|
|Connector_50_Outpost24|Pull information about outscan findings from Outpost24. Note: whitelist filter works with "productName" parameter.|False|
|Connector_32_PaloAltoPrismaCloud|Pull alerts from Palo Alto Prisma Cloud. Dynamic List works with the “policy.name” parameter.|False|
|Connector_47_Phishrod|Pull information about incidents from PhishRod. Note: dynamic list filter works with “emailSubject” parameter.|False|
|Connector_22_QRadar|Qradar Baseline Offenses connector used to fetch offenses and create Chronicle SOAR alerts based on the Qradar offenses names. Connector will create a single SOAR alert per Qradar offense, and will not try to create additional SOAR alerts with new events from Qradar. Connector uses SOAR dynamic list, but by default if no whitelist rules are set, it will fetchingest all offenses returned from the Qradar API offenses. Connector requires Qradar API version 10.1 or higher.|False|
|Connector_38_QualysVM|Pull detections from Qualys VM. Note: whitelist works with "Type" parameter.|True|
|Connector_24_RSANetWitness|RSA Netwitness static query connector.|False|
|Connector_29_Rapid7InsightIDR|This connector was built using API endpoints that are in preview release. Pull information about investigation from Rapid7 InsightIDR. Note: Dynamic list filter works with the "title" parameter.|True|
|Connector_16_Site24x7|Pull information about alert logs from Site24x7.|False|
|Connector_15_Sophos|Pull alerts from Sophos Central into Siemplify. Note: alerts are available to API only for 24 hours.|True|
|Connector_17_Splunk|Splunk Pull Connector|True|
|Connector_14_StellarCyberStarlight|Pull security events from Stellar Cyber Starlight.  Note: dynamic list works with the Chronicle SOAR alert name, which can be either “event_category: event_name” or “_source_xdr_event_xdr_killchain_stage:_source_xdr_event_name”|True|
|Connector_11_SumoLogicCloudSIEM|Pull information about insights from Sumo Logic Cloud SIEM. Note: dynamic list filter works with "name" parameter.|True|
|Connector_12_Sumologic|Sumologic Connector|True|
|Connector_10_SymantecATP|Fetch incidents from Symantec ATP|False|
|Connector_9_SymantecICDX|Fetching events from SymantecICDX server using a query|False|
|Connector_13_SysdigSecure|Use the Sysdig Secure - Events Connector to pull events from Sysdig Secure. The dynamic list works with the "ruleName" parameter.|True|
|Connector_7_TenableIO|Pull vulnerabilities from Tenable.io. Note: connector works with plugin families in whitelist.|True|
|Connector_8_TenableSecurityCenter|Tenable Security Center Connector|False|
|Connector_6_TrendVisionOne|Pull information about workbench alerts from Trend Vision One. Note: dynamic list filter works with "model" parameter.|True|
|Connector_4_VaronisDataSecurityPlatform|Connector can be used to fetch alerts from the Varonis Data Security Platform. The connector dynamic list can be used to filter specific alerts for ingestion based on the Varonis Data Security Platform alert name.|True|
|Connector_3_Vectra|Vectra - Detections Connector|True|
|Connector_5_VirusTotalV3|Pull information about Livehunt notifications and related files from VirusTotal. Note: this connector requires a premium API token. Dynamic list works with "rule_name" parameter.|True|
|Connector_2_Zabbix|Zabbix connector - fetches events from Zabbix.|False|


## Playbooks
|Name|Description|
|----|-----------|
|AWS EC2 Containment|This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.|
|AWS EC2 Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|AWS Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|AWS Users Containment|An embedded workflow that can receive inputs and return an output.|
|Amazon Web Services Cloud Platform Starting Playbook|Amazon Web Services Cloud Platform Starting Playbook provides reference implementation of how Amazon Web Services Cloud Platform alerts can be processed in Google SecOps.|
|Copy of AWS EC2 Containment|This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.|
|Copy of AWS EC2 Containment - 2|This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.|
|Copy of AWS EC2 Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|Copy of AWS EC2 Enrichment - 2|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|Copy of AWS Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|Copy of AWS Enrichment - 2|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|Copy of AWS Users Containment|An embedded workflow that can receive inputs and return an output.|
|Copy of AWS Users Containment - 2|An embedded workflow that can receive inputs and return an output.|
|Copy of Amazon Web Services Cloud Platform Starting Playbook|Amazon Web Services Cloud Platform Starting Playbook provides reference implementation of how Amazon Web Services Cloud Platform alerts can be processed in Google SecOps.|
|Copy of Amazon Web Services Cloud Platform Starting Playbook - 2|Amazon Web Services Cloud Platform Starting Playbook provides reference implementation of how Amazon Web Services Cloud Platform alerts can be processed in Google SecOps.|
|Copy of Copy of AWS EC2 Containment|This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.|
|Copy of Copy of AWS EC2 Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|Copy of Copy of AWS Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|Copy of Copy of AWS Users Containment|An embedded workflow that can receive inputs and return an output.|
|Copy of Copy of Amazon Web Services Cloud Platform Starting Playbook|Amazon Web Services Cloud Platform Starting Playbook provides reference implementation of how Amazon Web Services Cloud Platform alerts can be processed in Google SecOps.|
|Copy of Copy of Copy of New Playbook||
|Copy of Copy of CrowdStrike Containment|This block allows the playbook to perform containment actions on endpoints by targeting the IPs and hostnames associated with the case, helping to prevent further compromise during incident response.|
|Copy of Copy of CrowdStrike Falcon Starting Playbook|CrowdStrike Falcon Starting Playbook provides reference implementation of how CrowdStrike Falcon alerts can be processed in Google SecOps.|
|Copy of Copy of GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Copy of Copy of GTI Enrichment - 1|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Copy of Copy of Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Copy of Copy of Google SecOps Enrichment - 1|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Copy of Copy of Google Workspace Enrichment|This block enriches user entities with relevant information from Google Workspace, providing additional context to support investigation and response activities.|
|Copy of Copy of High Risk Users Check|This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.|
|Copy of Copy of MITRE Enrichment|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|Copy of Copy of New Playbook||
|Copy of Copy of New Playbook - 2||
|Copy of Copy of New Playbook - 2 - 2||
|Copy of CrowdStrike Containment|This block allows the playbook to perform containment actions on endpoints by targeting the IPs and hostnames associated with the case, helping to prevent further compromise during incident response.|
|Copy of CrowdStrike Containment - 2|This block allows the playbook to perform containment actions on endpoints by targeting the IPs and hostnames associated with the case, helping to prevent further compromise during incident response.|
|Copy of CrowdStrike Falcon Starting Playbook|CrowdStrike Falcon Starting Playbook provides reference implementation of how CrowdStrike Falcon alerts can be processed in Google SecOps.|
|Copy of CrowdStrike Falcon Starting Playbook - 2|CrowdStrike Falcon Starting Playbook provides reference implementation of how CrowdStrike Falcon alerts can be processed in Google SecOps.|
|Copy of GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Copy of GTI Enrichment - 1|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Copy of GTI Enrichment - 1 - 2|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Copy of GTI Enrichment - 2|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Copy of Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Copy of Google SecOps Enrichment - 1|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Copy of Google SecOps Enrichment - 1 - 2|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Copy of Google SecOps Enrichment - 2|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Copy of Google Workspace Enrichment|This block enriches user entities with relevant information from Google Workspace, providing additional context to support investigation and response activities.|
|Copy of Google Workspace Enrichment - 2|This block enriches user entities with relevant information from Google Workspace, providing additional context to support investigation and response activities.|
|Copy of High Risk Users Check|This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.|
|Copy of High Risk Users Check - 2|This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.|
|Copy of MITRE Enrichment|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|Copy of MITRE Enrichment - 2|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|Copy of New Block|An embedded workflow that can receive inputs and return an output.|
|Copy of New Playbook||
|Copy of New Playbook - 2||
|Copy of New Playbook - 3||
|CrowdStrike Containment|This block allows the playbook to perform containment actions on endpoints by targeting the IPs and hostnames associated with the case, helping to prevent further compromise during incident response.|
|CrowdStrike Falcon Starting Playbook|CrowdStrike Falcon Starting Playbook provides reference implementation of how CrowdStrike Falcon alerts can be processed in Google SecOps.|
|GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|GTI Enrichment - 1|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Google SecOps Enrichment - 1|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Google Workspace Enrichment|This block enriches user entities with relevant information from Google Workspace, providing additional context to support investigation and response activities.|
|High Risk Users Check|This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.|
|MITRE Enrichment|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|New Block|An embedded workflow that can receive inputs and return an output.|
|New Playbook||
|Playbook1- block and widget||
|fresh New Block|An embedded workflow that can receive inputs and return an output.|
|fresh New Playbook||
|testing single block|An embedded workflow that can receive inputs and return an output.|


## Visual Families
|Name|Description|
|----|-----------|
|Copy of Copy of Visual Family 1|Test Description|
|Copy of Visual Family 1|Test Description|
|Generated Visual Family 1|Auto-generated description for Generated Visual Family 1|
|Generated Visual Family 10|Auto-generated description for Generated Visual Family 10|
|Generated Visual Family 11|Auto-generated description for Generated Visual Family 11|
|Generated Visual Family 12|Auto-generated description for Generated Visual Family 12|
|Generated Visual Family 13|Auto-generated description for Generated Visual Family 13|
|Generated Visual Family 14|Auto-generated description for Generated Visual Family 14|
|Generated Visual Family 15|Auto-generated description for Generated Visual Family 15|
|Generated Visual Family 16|Auto-generated description for Generated Visual Family 16|
|Generated Visual Family 17|Auto-generated description for Generated Visual Family 17|
|Generated Visual Family 18|Auto-generated description for Generated Visual Family 18|
|Generated Visual Family 19|Auto-generated description for Generated Visual Family 19|
|Generated Visual Family 2|Auto-generated description for Generated Visual Family 2|
|Generated Visual Family 20|Auto-generated description for Generated Visual Family 20|
|Generated Visual Family 21|Auto-generated description for Generated Visual Family 21|
|Generated Visual Family 22|Auto-generated description for Generated Visual Family 22|
|Generated Visual Family 23|Auto-generated description for Generated Visual Family 23|
|Generated Visual Family 24|Auto-generated description for Generated Visual Family 24|
|Generated Visual Family 25|Auto-generated description for Generated Visual Family 25|
|Generated Visual Family 26|Auto-generated description for Generated Visual Family 26|
|Generated Visual Family 27|Auto-generated description for Generated Visual Family 27|
|Generated Visual Family 28|Auto-generated description for Generated Visual Family 28|
|Generated Visual Family 29|Auto-generated description for Generated Visual Family 29|
|Generated Visual Family 3|Auto-generated description for Generated Visual Family 3|
|Generated Visual Family 30|Auto-generated description for Generated Visual Family 30|
|Generated Visual Family 31|Auto-generated description for Generated Visual Family 31|
|Generated Visual Family 32|Auto-generated description for Generated Visual Family 32|
|Generated Visual Family 33|Auto-generated description for Generated Visual Family 33|
|Generated Visual Family 34|Auto-generated description for Generated Visual Family 34|
|Generated Visual Family 35|Auto-generated description for Generated Visual Family 35|
|Generated Visual Family 36|Auto-generated description for Generated Visual Family 36|
|Generated Visual Family 37|Auto-generated description for Generated Visual Family 37|
|Generated Visual Family 38|Auto-generated description for Generated Visual Family 38|
|Generated Visual Family 39|Auto-generated description for Generated Visual Family 39|
|Generated Visual Family 4|Auto-generated description for Generated Visual Family 4|
|Generated Visual Family 40|Auto-generated description for Generated Visual Family 40|
|Generated Visual Family 41|Auto-generated description for Generated Visual Family 41|
|Generated Visual Family 42|Auto-generated description for Generated Visual Family 42|
|Generated Visual Family 43|Auto-generated description for Generated Visual Family 43|
|Generated Visual Family 44|Auto-generated description for Generated Visual Family 44|
|Generated Visual Family 45|Auto-generated description for Generated Visual Family 45|
|Generated Visual Family 46|Auto-generated description for Generated Visual Family 46|
|Generated Visual Family 47|Auto-generated description for Generated Visual Family 47|
|Generated Visual Family 48|Auto-generated description for Generated Visual Family 48|
|Generated Visual Family 49|Auto-generated description for Generated Visual Family 49|
|Generated Visual Family 5|Auto-generated description for Generated Visual Family 5|
|Generated Visual Family 50|Auto-generated description for Generated Visual Family 50|
|Generated Visual Family 51|Auto-generated description for Generated Visual Family 51|
|Generated Visual Family 52|Auto-generated description for Generated Visual Family 52|
|Generated Visual Family 53|Auto-generated description for Generated Visual Family 53|
|Generated Visual Family 54|Auto-generated description for Generated Visual Family 54|
|Generated Visual Family 55|Auto-generated description for Generated Visual Family 55|
|Generated Visual Family 56|Auto-generated description for Generated Visual Family 56|
|Generated Visual Family 57|Auto-generated description for Generated Visual Family 57|
|Generated Visual Family 58|Auto-generated description for Generated Visual Family 58|
|Generated Visual Family 59|Auto-generated description for Generated Visual Family 59|
|Generated Visual Family 6|Auto-generated description for Generated Visual Family 6|
|Generated Visual Family 60|Auto-generated description for Generated Visual Family 60|
|Generated Visual Family 7|Auto-generated description for Generated Visual Family 7|
|Generated Visual Family 8|Auto-generated description for Generated Visual Family 8|
|Generated Visual Family 9|Auto-generated description for Generated Visual Family 9|
|Visual Family 1|Test Description|
|v1alpha Test Family With Rule|Test Description|


## Jobs
|Name|Description|
|----|-----------|
|CA Close Ticket In CA For Closed Case|Sync closure of the tickets at the CA Desk Manager with Siemplify cases closure.|
|Job_1|Automated marketplace job 1 for QRadar|
|Job_10|Automated marketplace job 10 for ServiceNow|
|Job_11|Automated marketplace job 11 for Splunk|
|Job_12|Automated marketplace job 12 for Splunk|
|Job_13|Automated marketplace job 13 for QRadar|
|Job_14|Automated marketplace job 14 for SCCEnterprise|
|Job_15|Automated marketplace job 15 for SCCEnterprise|
|Job_16|Automated marketplace job 16 for SCCEnterprise|
|Job_17|Automated marketplace job 17 for SentinelOneV2|
|Job_18|Automated marketplace job 18 for SentinelOneV2|
|Job_19|Automated marketplace job 19 for ServiceNow|
|Job_2|Automated marketplace job 2 for SCCEnterprise|
|Job_20|Automated marketplace job 20 for ServiceNow|
|Job_21|Automated marketplace job 21 for ServiceNow|
|Job_22|Automated marketplace job 22 for ServiceNow|
|Job_23|Automated marketplace job 23 for Splunk|
|Job_24|Automated marketplace job 24 for Splunk|
|Job_25|Automated marketplace job 25 for QRadar|
|Job_26|Automated marketplace job 26 for SCCEnterprise|
|Job_27|Automated marketplace job 27 for SCCEnterprise|
|Job_28|Automated marketplace job 28 for SCCEnterprise|
|Job_29|Automated marketplace job 29 for SentinelOneV2|
|Job_3|Automated marketplace job 3 for SCCEnterprise|
|Job_30|Automated marketplace job 30 for SentinelOneV2|
|Job_31|Automated marketplace job 31 for ServiceNow|
|Job_32|Automated marketplace job 32 for ServiceNow|
|Job_33|Automated marketplace job 33 for ServiceNow|
|Job_34|Automated marketplace job 34 for ServiceNow|
|Job_35|Automated marketplace job 35 for Splunk|
|Job_36|Automated marketplace job 36 for Splunk|
|Job_37|Automated marketplace job 37 for QRadar|
|Job_38|Automated marketplace job 38 for SCCEnterprise|
|Job_39|Automated marketplace job 39 for SCCEnterprise|
|Job_4|Automated marketplace job 4 for SCCEnterprise|
|Job_40|Automated marketplace job 40 for SCCEnterprise|
|Job_41|Automated marketplace job 41 for SentinelOneV2|
|Job_42|Automated marketplace job 42 for SentinelOneV2|
|Job_43|Automated marketplace job 43 for ServiceNow|
|Job_44|Automated marketplace job 44 for ServiceNow|
|Job_45|Automated marketplace job 45 for ServiceNow|
|Job_46|Automated marketplace job 46 for ServiceNow|
|Job_47|Automated marketplace job 47 for Splunk|
|Job_48|Automated marketplace job 48 for Splunk|
|Job_49|Automated marketplace job 49 for QRadar|
|Job_5|Automated marketplace job 5 for SentinelOneV2|
|Job_50|Automated marketplace job 50 for SCCEnterprise|
|Job_6|Automated marketplace job 6 for SentinelOneV2|
|Job_7|Automated marketplace job 7 for ServiceNow|
|Job_8|Automated marketplace job 8 for ServiceNow|
|Job_9|Automated marketplace job 9 for ServiceNow|
|Sync Comments|Sync comments from CA Desk Manager to Siemplify.|
|Sync Incidents V2|Use the Sync Incidents V2 job to synchronize Google SecOps alerts with Microsoft Sentinel incidents. This job ensures that comments, statuses, and tags are synchronized bi-directionally between both systems. Note: Assignee and severity synchronization occurs exclusively from Microsoft Sentinel to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the Microsoft Sentinel Incident tag. This job only works on alerts from the Microsoft Azure Sentinel Incident Connector v2.|
|Sync Incidents|Deprecated. This job synchronizes Google SecOps Alerts and Microsoft Sentinel Incidents. It ensures that comments, status, and tags are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the “Microsoft Sentinel Incident” tag. If the alert didn’t originate from “Microsoft Azure Sentinel Incident Connector v2”,  you will need to add an “Incident_ID” context value to the case for the job to be able to find the correct information.|

