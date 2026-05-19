# IMPORT 1 - SecMon_Enrichment_and_Triage_Block
An embedded workflow that can receive inputs and return an output.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False



##### Input Parameters
|Name|Default Value|
|----|-------------|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Critical Ingestion Source Case tag |Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Critical Feed Name case tag |Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Change Case Name Connector|The action changes the case's name (title)|Tools|Change Case Name|
|Execute UDM query against connector|Execute custom UDM query in Google Chronicle. Note: 120 action executions are allowed per hour. Aggregated queries are supported only via Chronicle API configuration of integration.|GoogleChronicle|Execute UDM Query|
|Get connector Data Table |Check, if provided values are found in the data table in Google SecOps. Note: this action only works with Chronicle API authentication. Backstory API is not supported.|GoogleChronicle|Is Value In Data Table|
|Set Data Table name value   |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Assign case to unassigned (L0)|Assign case to specific user or usergroup|Siemplify|Assign Case|
|Converts data table time window value to negative seconds|This action will render a Jinja2 template using a JSON input.  |TemplateEngine|Render Template|
|UDM Query - Timestamp|Returns the current date and time |Tools|Get Current Time|
|Change Alert Priority_3|Automatically change the alert priority to the given input. Note: This action is compatible only with Siemplify version 5.6 and higher.|Siemplify|Change Alert Priority|
|Change Priority (PCI flow)|Automatically change case priority to the given input|Siemplify|Change Priority|
|PCI case tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Set Case SLA (PCI flow)|Set the SLA for a case. This action has the highest priority and it will override the existing SLA defined for the specific case.|Siemplify|Set Case SLA|
|Change Alert Priority_2|Automatically change the alert priority to the given input. Note: This action is compatible only with Siemplify version 5.6 and higher.|Siemplify|Change Alert Priority|
|Change Priority (Non-critical and Non-PCI)|Automatically change case priority to the given input|Siemplify|Change Priority|
|Set Case SLA (Non-critical and Non-PCI)|Set the SLA for a case. This action has the highest priority and it will override the existing SLA defined for the specific case.|Siemplify|Set Case SLA|
|Change Case Name Feedname|The action changes the case's name (title)|Tools|Change Case Name|
|Execute UDM query against feed name|Execute custom UDM query in Google Chronicle. Note: 120 action executions are allowed per hour. Aggregated queries are supported only via Chronicle API configuration of integration.|GoogleChronicle|Execute UDM Query|
|Get feedname Data Table |Check, if provided values are found in the data table in Google SecOps. Note: this action only works with Chronicle API authentication. Backstory API is not supported.|GoogleChronicle|Is Value In Data Table|
|Set Data Table name value |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Change Case Name Logtype|The action changes the case's name (title)|Tools|Change Case Name|
|Execute UDM query against log type|Execute custom UDM query in Google Chronicle. Note: 120 action executions are allowed per hour. Aggregated queries are supported only via Chronicle API configuration of integration.|GoogleChronicle|Execute UDM Query|
|Get logtype Data Table|Check, if provided values are found in the data table in Google SecOps. Note: this action only works with Chronicle API authentication. Backstory API is not supported.|GoogleChronicle|Is Value In Data Table|
|Set Data Table name value|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Common asset_type_value|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Change Alert Priority_1|Automatically change the alert priority to the given input. Note: This action is compatible only with Siemplify version 5.6 and higher.|Siemplify|Change Alert Priority|
|Change Priority (Critical flow)|Automatically change case priority to the given input|Siemplify|Change Priority|
|Set Case SLA (Critical flow)|Set the SLA for a case. This action has the highest priority and it will override the existing SLA defined for the specific case.|Siemplify|Set Case SLA|
|Close Case|Closes the case the current alert has been grouped to|Siemplify|Close Case|
|Set UDMQueryTimestamp variable|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Change Case Name Ingestion Source|The action changes the case's name (title)|Tools|Change Case Name|
|Execute UDM query against ingestion source|Execute custom UDM query in Google Chronicle. Note: 120 action executions are allowed per hour. Aggregated queries are supported only via Chronicle API configuration of integration.|GoogleChronicle|Execute UDM Query|
|Get ingestionsource Data Table |Check, if provided values are found in the data table in Google SecOps. Note: this action only works with Chronicle API authentication. Backstory API is not supported.|GoogleChronicle|Is Value In Data Table|
|Set Data Table name value  |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Calculates time window from GCP Monitoring alert timestamp|Convert a datetime value from one format to another format.  For GCP_MONITORING_ALERTS_CUSTOM change From Format to %Y-%m-%dT%H:%M:%S.%fZ|Functions|Convert Time Format|
|Common asset_type_value  |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Case Comment|Add a comment to the case the current alert has been grouped to|Siemplify|Case Comment|
|Get Case Comments|This action will get all the data from a case and return a JSON result.  The result includes comments, entity information, insights, playbooks that ran, alert information and events.|Tools|Get Case Comments|
|Common asset_type_value |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Nespresso case tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Critical Log Type case tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Critical Connector Case tag |Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Common asset_type_value   |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Set Case Comments variable|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|

