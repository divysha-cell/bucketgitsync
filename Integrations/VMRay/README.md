
# VMRay

VMRay Analyzer provides Malware Analysts and Incident Responders with a comprehensive picture of advanced threats in an intiutive interface.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://cloud.vmray.com|
|Api Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|hashID-3.1.4-py2.py3-none-any.whl|
|TIPCommon-1.0.11.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Add Tag to Submission
Add Tag to Submission using Submission ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Submission ID|The ID of the Submission.|True|String||
|Tag Name|The tag Name that need to be added.|True|String||



#### Upload File And Get Report
Submit files for analysis in VMRay. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sample File Path|Specify a comma-separated list of absolute file paths for submission.|True|String||
|Tag Names|Specify the tags that you want to add to the submission.|False|String||
|Comment|Specify the comment that you want to add to the submission.|False|String||



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Scan URL
Submit a URL and receive related information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat Indicator Score Threshold|Specify the lowest score that will be used to return threat indicators. Maximum: 5.|True|String|3|
|IOC Type Filter|Specify a comma-separated list of IOC types that need to be returned. Possible values: ips, urls, domains.|True|String|ips, urls, domains|
|IOC Verdict Filter|Specify a comma-separated list of IOC verdicts that will be used during the ingestion of IOCs. Possible values: Malicious, Suspicious, Clean, None.|True|String|Malicious, Suspicious|
|Max IOCs To Return|Specify how many IOCs to return per entity per IOC type. Default: 10.|False|String|10|
|Max Threat Indicators To Return|Specify how many threat indicators to return per entity. Default: 10.|False|String|10|
|Create Insight|If enabled, action will create an insight containing information about entities.|False|Boolean|true|
|Only Suspicious Insight|If enabled, action will only create insight for suspicious entities. Note: "Create Insight" parameter needs to be enabled.|False|Boolean|false|
|Tag Names|Specify the tags that you want to add to the submission.|False|String||
|Comment|Specify the comment that you want to add to the submission.|False|String||



##### JSON Results
```json
[{"Entity": "http://exmaple.com/", "EntityResult": {"sample_account_ids": ["7xx"], "sample_child_relations": [], "sample_child_relations_truncated": false, "sample_child_sample_ids": [], "sample_classifications": [], "sample_container_type": null, "sample_created": "2022-04-10T19:16:59", "sample_display_url": "http://exmaple.com", "sample_emailhash": null, "sample_filename": "sample.url", "sample_filesize": 18, "sample_highest_vti_score": 46, "sample_highest_vti_severity": "suspicious", "sample_id": "7297xxx", "sample_imphash": null, "sample_is_multipart": false, "sample_is_type_overridden": false, "sample_last_md_score": null, "sample_last_reputation_severity": null, "sample_last_vt_score": null, "sample_lnk_target": null, "sample_md5hash": "9f31ee4874ec49149a9ebxxxxxxxxxxx", "sample_parent_relations": [], "sample_parent_relations_truncated": false, "sample_parent_sample_ids": [], "sample_password": "NXxxxxxxxx", "sample_password_protected": false, "sample_pe_signature": null, "sample_priority": 3, "sample_score": 46, "sample_severity": "suspicious", "sample_sha1hash": "ea6f3aae785e5a6a0f7e7bcxxxxxxxxxxxxxxxxx", "sample_sha256hash": "3be93055b83dbcc4d515358f3eb655d503d63524b653xxxxxxxxxxxxxxxxxxxx", "sample_ssdeephash": "3:N1KbKxxx:xx", "sample_temporary": false, "sample_threat_names": [], "sample_type": "URL", "sample_unsupported_type": null, "sample_url": "http://exmaple.com", "sample_verdict": "suspicious", "sample_verdict_migrated": true, "sample_verdict_reason_code": null, "sample_verdict_reason_description": null, "sample_vti_score": "suspicious", "sample_webif_url": "https://cloud.vmray.com/samples/7297xxx", "iocs": {"domains": [], "emails": [], "files": [], "ips": [], "mutexes": [], "processes": [], "registry": [], "urls": [{"analysis_ids": ["8961xxx", "8960xxx"], "categories": ["Contacted"], "content_types": ["text/html"], "countries": [], "country_codes": [], "id": 0, "ioc": true, "ioc_type": "url", "ip_addresses": ["104.18.xxx.xx", "104.18.xxx.xx"], "methods": ["GET"], "numeric_severity": 3, "original_urls": ["http://exmaple.com/favicon.ico"], "parent_files": [], "parent_processes": [], "parent_processes_ids": [], "parent_processes_names": [], "referrers": ["http://exmaple.com/"], "severity": "suspicious", "sources": ["Pcap", "Web Engine"], "type": "url_artifact", "url": "http://exmaple.com/favicon.ico", "user_agents": ["Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36"], "verdict": "suspicious", "verdict_reason_code": null, "verdict_reason_description": "", "version": 3}]}, "threat_indicators": [{"analysis_ids": ["8959xxx", "8959xxx"], "category": "Heuristics", "classifications": [], "id": "74202xxx", "operation": "Suspicious page characteristics", "score": 1}]}}]
```



#### Scan Hash
Get details about a specific hash.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat Indicator Score Threshold|Specify the lowest score that will be used to return threat indicators. Maximum: 5.|True|String|3|
|IOC Type Filter|Specify a comma-separated list of IOC types that need to be returned. Possible values: domains, emails, files, ips, mutexes, processes, registry, urls.|True|String|ips, files, emails, urls, domains|
|IOC Verdict Filter|Specify a comma-separated list of IOC verdicts that will be used during the ingestion of IOCs. Possible values: Malicious, Suspicious, Clean, None.|True|String|Malicious, Suspicious|
|Max IOCs To Return|Specify how many IOCs to return per entity per IOC type. Default: 10.|False|String|10|
|Max Threat Indicators To Return|Specify how many threat indicators to return per entity. Default: 10.|False|String|10|
|Create Insight|If enabled, action will create an insight containing information about entities.|False|Boolean|true|
|Only Suspicious Insight|If enabled, action will only create insight for suspicious entities. Note: "Create Insight" parameter needs to be enabled.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "a4b19054d162aab80227xxxxxxxxxxxxxxxxxxxx", "EntityResult": {"sample_account_ids": ["7xx"], "sample_child_relations": [], "sample_child_relations_truncated": false, "sample_child_sample_ids": [], "sample_classifications": [], "sample_container_type": null, "sample_created": "2019-06-05T07:29:05", "sample_display_url": "http://test.com/test.php", "sample_emailhash": null, "sample_filename": "sample.url", "sample_filesize": 35, "sample_highest_vti_score": 80, "sample_highest_vti_severity": "malicious", "sample_id": "3945xxx", "sample_imphash": null, "sample_is_multipart": false, "sample_is_type_overridden": false, "sample_last_md_score": null, "sample_last_reputation_severity": "malicious", "sample_last_vt_score": null, "sample_lnk_target": null, "sample_md5hash": "de765a6a9931xxxxxxxxxxxxxxxxxxxx", "sample_parent_relations": [], "sample_parent_relations_truncated": false, "sample_parent_sample_ids": [], "sample_password": "PlrQxxxxxx", "sample_password_protected": false, "sample_pe_signature": null, "sample_priority": 3, "sample_score": 80, "sample_severity": "malicious", "sample_sha1hash": "a4b19054d162aab80227xxxxxxxxxxxxxxxxxxxx", "sample_sha256hash": "8fb5c7a88058fad398dfe290f3821a3983a608abe6b3xxxxxxxxxxxxxxxxxxxx", "sample_ssdeephash": "3:N1KTxKWixxxxxx:C1Nxxx", "sample_temporary": false, "sample_threat_names": ["C2/Generic-A"], "sample_type": "URL", "sample_unsupported_type": null, "sample_url": "http://test.com/test.php", "sample_verdict": "malicious", "sample_verdict_migrated": true, "sample_verdict_reason_code": null, "sample_verdict_reason_description": null, "sample_vti_score": "malicious", "sample_webif_url": "https://cloud.vmray.com/samples/3945xxx", "iocs": {"domains": [], "emails": [], "files": [], "ips": [], "urls": [{"analysis_ids": ["7904xxx", "7904xxx"], "categories": ["Sample"], "content_types": [], "countries": ["United States"], "country_codes": ["US"], "id": 0, "ioc": true, "ioc_type": "url", "ip_addresses": ["99.83.xxx.xxx"], "methods": ["GET"], "numeric_severity": 4, "original_urls": ["http://test.com/test.php"], "parent_files": [], "parent_processes": [], "parent_processes_ids": [], "parent_processes_names": [], "referrers": [], "severity": "malicious", "sources": ["Pcap", "Web Engine"], "type": "url_artifact", "url": "http://test.com/test.php", "user_agents": ["Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36"], "verdict": "malicious", "verdict_reason_code": null, "verdict_reason_description": "", "version": 3}]}, "threat_indicators": [{"analysis_ids": ["7904xxx", "7904xxx"], "category": "Reputation", "classifications": [], "id": "7420xxxx", "operation": "Known malicious URL", "score": 4}]}}]
```









