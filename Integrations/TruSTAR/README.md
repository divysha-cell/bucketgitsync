
# TruSTAR

TruSTAR is an intelligence management platform that transforms and automates data for security operations teams and tools.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://api.trustar.co|
|API Key||True|String||
|API Secret||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich entities using information from TruSTAR. Supported entities: All.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Level Threshold|Specify what should be the lowest security level for the entity to be marked as suspicious.|True|List|Low|
|Enclave Filter|Specify a comma-separated list of enclave names that should be used during the enrichment.|False|String||



##### JSON Results
```json
[{"Entity": "http://xxxxx.com/xxxx/wp-xxx/", "EntityResult": {"indicatorType": "URL", "value": "http://xxxxx.com/xxxx/xxxx-xxxx/", "correlationCount": 0, "priorityLevel": "NOT_FOUND", "noteCount": 0, "sightings": 1, "firstSeen": 1618050696988, "lastSeen": 1618050696988, "enclaveIds": ["xxxx-xxxxx-xxxx-xxxx-xxxx"], "tags": [], "source": "", "notes": [], "guid": "URL|http://xxxxx.com/xxxxx/xxxx-xxxx/", "summaries": [{"reportId": "xxxxx-xxxx-xxxx-xxxx-xxxx", "updated": 1618040000000, "enclaveId": "xxxxx-xxxx-xxxx-xxxx-xxxx", "source": {"key": "virustotal", "name": "VirusTotal"}, "type": "URL", "value": "http://xxxxx.com/xxx/xxxxx-xxxxx/", "score": {"name": "Positives/Total Scans", "value": "13/85"}, "attributes": [{"name": "Websites with Positive Detections", "value": ["AlienVault", "Avira", "BitDefender", "CLEAN MX", "CRDF", "CyRadar", "ESET", "Emsisoft", "Fortinet", "Google Safebrowsing", "Kaspersky", "Netcraft", "Sophos"]}, {"name": "Scan Date", "value": 123456}], "severityLevel": 1}]}}, {"Entity": "http://xxxxx.xxxx/xxxxx/xxxx.exe", "EntityResult": {"indicatorType": "URL", "value": "http://xxxxx.xxxxx/xxxxx/xxxx.xxxx", "correlationCount": 0, "priorityLevel": "NOT_FOUND", "noteCount": 0, "sightings": 1, "firstSeen": 1617923344643, "lastSeen": 1617923344643, "enclaveIds": ["xxxxx-xxxx-xxxx-xxxx-xxxx"], "tags": [], "source": "", "notes": [], "guid": "URL|http://xxxx.xxxx/xxxx/xxxx.xxxx", "summaries": [{"reportId": "xxxx-xxxx-xxxx-xxxx-xxxx", "updated": 1617900133000, "enclaveId": "xxxx-xxxx-xxxx-xxxx-xxxxx", "source": {"key": "virustotal", "name": "VirusTotal"}, "type": "URL", "value": "xxxxx://xxxxx.xxxx/xxxxx/xxxxx.exe", "score": {"name": "Positives/Total Scans", "value": "12/85"}, "attributes": [{"name": "Websites with Positive Detections", "value": ["AegisLab WebGuard", "AlienVault", "CRDF", "ESET", "Emsisoft", "Fortinet", "G-Data", "Kaspersky", "Spamhaus", "URLhaus", "VX Vault", "benkow.cc"]}, {"name": "Scan Date", "value": 123456}], "severityLevel": 1}]}}]
```



#### Get Related IOCs
Get information about IOCs that are related to the provided entities. Supported entities: All.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max IOCs To Return|Specify how many IOCs to return. Default: 50. Maximum: 1000.|False|String|50|
|Enclave Filter|Specify a comma-separated list of enclave names that should be used during the enrichment.|False|String||



##### JSON Results
```json
[{"SOFTWARE": ["X:\\XXXXXXX\\XXXXXXXX\\XXXXXX.XXX"], "URL": ["XXXXXX.XXX.XXXX"], "IP": ["X.X.X.X"], "EMAIL_ADDRESS": ["XXXX@XXXX.XXXX.XXXXX"], "MD5": ["XXXXXXXXXXXXXXXXXXXXXX"], "SHA1": ["XXXXXXXXXXXXXXXXXXXXXX"], "CIDR_BLOCK": ["XXX.XX.XX.XX/XX"]}]
```



#### Ping
Test connectivity to the TruSTAR with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Get Related Reports
Get information about reports related to the entities. Supported entities: All.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight containing information about reports related to the entities.|False|Boolean|true|
|Include Report Body In Insight|If enabled, insight will contain information about the report body. Note: report body can be very big in size.|False|Boolean|false|
|Enclave Filter|Specify a comma-separated list of enclave names that should be used during the enrichment.|False|String||
|Max Reports To Return|Specify how many reports to return. Default: 10. Maximum: 25.|False|String|10|



##### JSON Results
```json
[{"id": "XXXXXX-XXXX-XXXXX-XXXXX-XXXXXXXXXX", "created": "XXXXXXXXXXXXXXX", "updated": "XXXXXXXXXXXXXXX", "title": "XXXXX", "distributionType": "XXXXXXXX", "submissionStatus": "XXXXXXXX", "timeBegan": "XXXXXXXXXXXXXXX", "reportBody": "XXXXXXXXXX", "externalTrackingId": "XXXXXX-XXXXXX-XXXXX", "enclaveIds": [], "tags": [{"guid": "XXXXXXX XXXXXXX", "name": "XXXXXXX XXXXXXX", "enclaveId": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXX"}]}]
```



#### List Enclaves
List available enclaves in TruSTAR.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter.|False|String||
|Max Enclaves To Return|Specify how many enclaves to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"name": "XXXXXX", "templateName": "XXXXXXX", "workflowSupported": "False", "read": "True", "create": "False", "update": "False", "id": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX", "type": "XXXXXXX"}]
```









