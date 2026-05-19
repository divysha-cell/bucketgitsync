# Amazon Web Services Cloud Platform Starting Playbook
Amazon Web Services Cloud Platform Starting Playbook provides reference implementation of how Amazon Web Services Cloud Platform alerts can be processed in Google SecOps.



**Enabled:** False

**Version:** 0

**Type:** Playbook

**Priority:** 3

**Playbook Simulator:** False



### Playbook Trigger
**Trigger Type:** Custom Trigger

**Conditions Operator:** Or

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
|[Alert.Name]|Starts With|AWS|
|[Event.event_metadata_productName]|Contains|AWS|
|[Event.event_metadata_vendorName]|Contains|AMAZON|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Rule Name Tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Change Case Name|The action changes the case's name (title)|Tools|Change Case Name|
|Reset REMEDIATION Variable|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Summary |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Close Alert|Closes the current alert|Siemplify|Close Alert|
|Alert Overview|Fetch information about a detection in Google Chronicle.|GoogleChronicle|Get Detection Details|
|Change Stage to Assesment|Change case stage to handling|Siemplify|Change Case Stage|
|Tag Cloud|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|AWS TAG|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|

### Involved Blocks
|Name|Description|
|----|-----------|
|AWS Enrichment|This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.|
|AWS Users Containment|An embedded workflow that can receive inputs and return an output.|
|GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
|AWS EC2 Containment|This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.|
|MITRE Enrichment|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|Set Initial Severity|This block sets the initial alert score based on the SIEM detection severity or the rule metadata severity label.|
|Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Alert Priority|This block sets the alert priority using a previously defined playbook variable, ensuring consistent prioritization logic for the case workflow.|
