# GitSync

## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Connector_Instance_1|Automated connector 1|True|
|Connector_Instance_15|Automated connector 15|True|
|Connector_Instance_29|Automated connector 29|True|
|Connector_Instance_43|Automated connector 43|True|
|Test_Connector_VT_1|Test connector|True|
|Connector_Instance_14|Automated connector 14|True|
|Connector_Instance_28|Automated connector 28|True|
|Connector_Instance_42|Automated connector 42|True|
|Connector_Instance_11|Automated connector 11|True|
|Connector_Instance_25|Automated connector 25|True|
|Connector_Instance_39|Automated connector 39|True|
|Connector_Instance_12|Automated connector 12|True|
|Connector_Instance_26|Automated connector 26|True|
|Connector_Instance_40|Automated connector 40|True|
|Connector_Instance_10|Automated connector 10|False|
|Connector_Instance_24|Automated connector 24|False|
|Connector_Instance_38|Automated connector 38|False|
|Connector_Instance_23|Automated connector 23|False|
|Connector_Instance_37|Automated connector 37|False|
|Connector_Instance_9|Automated connector 9|False|
|Connector_Instance_13|Automated connector 13|True|
|Connector_Instance_27|Automated connector 27|True|
|Connector_Instance_41|Automated connector 41|True|
|Connector_Instance_21|Automated connector 21|True|
|Connector_Instance_35|Automated connector 35|True|
|Connector_Instance_49|Automated connector 49|True|
|Connector_Instance_7|Automated connector 7|True|
|Connector_Instance_22|Automated connector 22|False|
|Connector_Instance_36|Automated connector 36|False|
|Connector_Instance_50|Automated connector 50|False|
|Connector_Instance_8|Automated connector 8|False|
|Connector_Instance_20|Automated connector 20|True|
|Connector_Instance_34|Automated connector 34|True|
|Connector_Instance_48|Automated connector 48|True|
|Connector_Instance_6|Automated connector 6|True|
|Connector_Instance_19|Automated connector 19|True|
|Connector_Instance_33|Automated connector 33|True|
|Connector_Instance_47|Automated connector 47|True|
|Connector_Instance_5|Automated connector 5|True|
|Connector_Instance_18|Automated connector 18|True|
|Connector_Instance_32|Automated connector 32|True|
|Connector_Instance_4|Automated connector 4|True|
|Connector_Instance_46|Automated connector 46|True|
|Connector_Instance_16|Automated connector 16|True|
|Connector_Instance_2|Automated connector 2|True|
|Connector_Instance_30|Automated connector 30|True|
|Connector_Instance_44|Automated connector 44|True|
|Connector_Instance_17|Automated connector 17|False|
|Connector_Instance_3|Automated connector 3|False|
|Connector_Instance_31|Automated connector 31|False|
|Connector_Instance_45|Automated connector 45|False|


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
|fresh New Block|An embedded workflow that can receive inputs and return an output.|
|fresh New Playbook||


## Jobs
|Name|Description|
|----|-----------|
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

