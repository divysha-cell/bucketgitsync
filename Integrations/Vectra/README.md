
# Vectra

Designed by an award-winning team of data scientists and threat researchers, Vectra represents the rich, security-enriched data output of a holistic approach to security â€“ capturing network metadata at scale, enriching it with machine learning-derived security information.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|URL|https://<address>:<port>|
|API Token||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Update Note
Update note for the endpoint or detection.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Item Type|Select on which item type you want to update a note.|True|List|Endpoint|
|Item ID|Specify ID of the detection/endpoint.|True|String||
|Note|Specify what note you want to have on the detection/endpoint.|True|String||



#### Enrich Endpoint
Fetch endpoint's system information by its hostname or IP address.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"host_luid": "hMslFCxx", "privilege_category": null, "ip": "10.0.2.xx", "privilege_level": null, "note_modified_by": "siemplify", "is_targeting_key_asset": false, "note_modified_timestamp": "2020-06-06T05:08:47Z", "key_asset": false, "t_score": 26, "id": 100000, "note": "fdsf", "detection_profile": "IT Discovery", "severity": "low", "previous_ips": ["10.0.2.xx"], "state": "active", "sensor": "YLq09axx", "assigned_date": null, "has_active_traffic": false, "targets_key_asset": false, "tags": [], "host_session_luids": ["6ia151xx", "B6O2N6xx"], "last_source": "10.0.2.xx", "last_detection_timestamp": "2020-05-26T19:18:58Z", "last_modified": "2020-06-06T05:08:47Z", "groups": [], "host_artifact_set": [{"vendor": "Intel Corp", "source": null, "type": "mac", "siem": false, "value": "4c:1d:96:22:29:00"}, {"source": null, "type": "dhcp", "siem": false, "value": "DESKTOP-9993xxx"}], "host_url": "https://70.54.200.xxx:64443/api/v2.1/hosts/xxx", "has_custom_model": false, "detection_set": ["https://70.54.200.xxx:64443/api/v2.1/detections/xx"], "sensor_name": "Vectra X", "name": "DESKTOP-9993xxx", "url": "https://70.54.200.xxx:64443/api/v2.1/hosts/xxx", "certainty": 27, "probable_owner": null, "c_score": 27, "is_key_asset": false, "threat": 26, "assigned_to": null, "active_traffic": false}, "Entity": "DESKTOP-9993xxx"}]
```



#### Update Detection Status
Update status of the detection.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection ID|Specify the detection ID on which you want to update the status.|True|String||
|Status|Specify what status to set on the detection.|True|List|Fixed|



#### Ping
Test connectivity to Vectra with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds



#### Remove Tags
Remove tags from the endpoint or detection in Vectra.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Item Type|Select from which item type you want to remove tags.|True|List|Endpoint|
|Item ID|Specify ID of the detection/endpoint.|True|String||
|Tags|Specify what tags you want to remove from detection/endpoint. Tags should be separated by comma, e.g tag1, tag2.|True|String||



#### Add Tags
Add tags to the endpoint or detection in Vectra.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Item Type|Select to which item type you want to add tags.|True|List|Endpoint|
|Item ID|Specify ID of the detection/endpoint.|True|String||
|Tags|Specify what tags you want to add to detection/endpoint. Tags should be separated by comma, e.g tag1, tag2. |True|String||



#### Get Triage Rule Details
Get detailed information about triage rules.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Triage Rule IDs|Specify a comma-separated list of triage rule IDs. Example: 28,29.|True|String||
|Create Insights|If enabled, action will create a separate insight for every processed triage rule.|False|Boolean|true|



##### JSON Results
```json
[{"detection": "Hidden HTTPS Tunnel", "description": "whatever", "last_timestamp": "2020-10-04T00:00:10Z", "url": "https://api.demo.vectranetworks.com/api/v2.1/rules/28", "source_conditions": {"OR": [{"AND": [{"ANY_OF": {"field": "host", "values": [{"url": "https://api.demo.vectranetworks.com/api/v2.1/hosts/142", "value": 142, "label": "IP-10.10.100.10"}], "groups": [], "label": "Host"}}]}]}, "is_whitelist": false, "enabled": true, "detection_category": "COMMAND & CONTROL", "total_detections": 2, "priority": 1, "triage_category": "triage rule 1", "template": false, "created_timestamp": "2020-10-01T17:21:19Z", "active_detections": 2, "id": 28, "additional_conditions": {"OR": [{"AND": [{"ANY_OF": {"field": "remote1_ip", "values": [{"url": null, "value": "35.166.75.118", "label": "35.166.75.118"}], "groups": [], "label": "C&C Server IP"}}]}]}}, {"detection": "Hidden HTTPS Tunnel", "description": "Expected behavior from Slack collaboration", "last_timestamp": null, "url": "https://api.demo.vectranetworks.com/api/v2.1/rules/29", "source_conditions": null, "is_whitelist": false, "enabled": true, "detection_category": "COMMAND & CONTROL", "total_detections": 0, "priority": 2, "triage_category": "Slack Tunnel", "template": false, "created_timestamp": "2020-10-08T07:10:53Z", "active_detections": 0, "id": 29, "additional_conditions": {"OR": [{"AND": [{"ANY_OF": {"field": "remote1_dns", "values": [], "groups": [{"url": "https://api.demo.vectranetworks.com/api/v2.1/groups/18", "value": 18, "label": "Cognito - Slack"}], "label": "C&C Server Domain"}}]}]}}]
```









## Connectors
#### Vectra - Detections Connector
Vectra - Detections Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Vectra server.|True|String|https://x.x.x.x:x|
|API Token|API token of the Vectra account.|True|Password|*****|
|Lowest Threat Score To Fetch|Lowest threat score that will be used to fetch detections. Min:0 Max:100|True|Int|50|
|Lowest Certainty Score To Fetch|Lowest certainty score that will be used to fetch detections. Min: 0 Max: 100|False|Int|0|
|Category Filter|Specify which categories of detections to ingest into Siemplify. Possible values: Command & Control  Botnet  Reconnaissance  Lateral Movement  Exfiltration  Info|False|String|Command & Control, Botnet, Reconnaissance, Lateral Movement, Exfiltration, Info|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve threats from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Detections To Fetch|How many detections to process per one connector iteration. Limit is 5000. This is a Vectra limitation.|False|Int|25|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Vectra server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




