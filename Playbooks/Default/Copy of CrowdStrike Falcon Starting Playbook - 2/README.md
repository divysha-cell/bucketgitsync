# Copy of CrowdStrike Falcon Starting Playbook - 2
CrowdStrike Falcon Starting Playbook provides reference implementation of how CrowdStrike Falcon alerts can be processed in Google SecOps.



**Enabled:** False

**Version:** 0

**Type:** Playbook

**Priority:** 3

**Playbook Simulator:** False



### Playbook Trigger
**Trigger Type:** Custom Trigger

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
|[Event.event_metadata_vendorName]|Contains|Crowdstrike
|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Close Alert|Closes the current alert|Siemplify|Close Alert|
|Set Initial Summary|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|EDR Tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Change Case Name|The action changes the case's name (title)|Tools|Change Case Name|
|Rule Name Tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|CrowdStrike Tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Change Stage to Assesment|Change case stage to handling|Siemplify|Change Case Stage|

### Involved Blocks
|Name|Description|
|----|-----------|
|Alert Priority|This block sets the alert priority using a previously defined playbook variable, ensuring consistent prioritization logic for the case workflow.|
|High Risk Users Check|This block checks Google GTI sourced alerts against a SOAR custom list to find matches of targeted Industries.|
|GTI Enrichment - 1|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|Google Workspace Enrichment|This block enriches user entities with relevant information from Google Workspace, providing additional context to support investigation and response activities.|
|Set Initial Severity|This block sets the initial alert score based on the SIEM detection severity or the rule metadata severity label.|
|Google SecOps Enrichment - 1|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|CrowdStrike Containment|This block allows the playbook to perform containment actions on endpoints by targeting the IPs and hostnames associated with the case, helping to prevent further compromise during incident response.|
