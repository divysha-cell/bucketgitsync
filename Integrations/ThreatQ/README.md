
# ThreatQ

A threat intelligence platform designed to accelerate security operations.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ServerAddress|None|True|IP|xx.xx.xx.xx|
|ClientId|None|True|String||
|Username|None|True|String||
|Password|None|True|Password|*****|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|urllib3-2.2.1-py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|


## Actions
#### Update Indicator Score
Action updates indicator score in ThreatQ
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Score|Specify the new score of the indicator.|True|List|7 - Medium|
|Score Validation|Specify what kind of score validation should be used. If “ Highest Score” is specified, action will compare current values and update the indicator’s score only, if the specified score is higher than current generated and manual score. If “Force Update” is specified, action will update the indicator's score without comparing current values.|True|List|Highest Score|



##### JSON Results
```json
[{"EntityResult": {"data": {"created_at": "2020-08-13 16:56:45", "updated_at": "2020-08-18 14:08:43", "generated_score": "0.00", "indicator_id": 2145, "score_config_hash": "7f8b888a2d2b462310d5227aa75exxxa78973a96", "manual_score": "7"}}, "Entity": "98.158.000.000"}, {"EntityResult": {"data": {"created_at": "2020-07-30 11:17:43", "updated_at": "2020-08-18 13:57:32", "generated_score": "0.00", "indicator_id": 58, "score_config_hash": "7f8b888a2d2b462310d5227axxxe8c4a78973a96", "manual_score": "7"}}, "Entity": "admin2@email.com"}, {"EntityResult": {"data": {"created_at": "2020-07-30 11:19:10", "updated_at": "2020-08-18 13:57:34", "generated_score": "0.00", "indicator_id": 60, "score_config_hash": "7f8xxx8a2d2b462310d5227aa75e8c4a78973a96", "manual_score": "7"}}, "Entity": "HTTP://example.COM/F1Q7QX.PHP"}, {"EntityResult": {"data": {"created_at": "2020-07-30 11:17:42", "updated_at": "2020-08-18 13:57:37", "generated_score": "0.00", "indicator_id": 57, "score_config_hash": "7f8b888a2d2xxx2310d5227aa75e8c4a78973a96", "manual_score": "7"}}, "Entity": "admin@email.com"}, {"EntityResult": {"data": {"created_at": "2020-07-30 11:19:12", "updated_at": "2020-08-18 13:57:40", "generated_score": "0.00", "indicator_id": 63, "score_config_hash": "7f8b888a2d2b462310dxxx7aa75e8c4a78973a96", "manual_score": "7"}}, "Entity": "YOUR NEW SALARY NOTIFICATION"}, {"EntityResult": {"data": {"created_at": "2020-07-19 09:17:43", "updated_at": "2020-08-18 13:57:42", "generated_score": "0.00", "indicator_id": 2, "score_config_hash": "7f8b888a2d2b462310d5227aa75e8c4a78973xxx", "manual_score": "7"}}, "Entity": "7815696ecbf1c96e6894b779456d3xxx"}, {"EntityResult": {"data": {"created_at": "2020-08-13 16:56:44", "updated_at": "2020-08-18 13:57:45", "generated_score": "0.00", "indicator_id": 2075, "score_config_hash": "7f8b888a2d2b462310d5227aa75e8c4a78973a96", "manual_score": "7"}}, "Entity": "91.217.000.000"}]
```



#### Create Object
Create an object in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|Specify to which object type attribute should be added.|True|List|Attack Pattern|
|Value|Specify the value of the new object.|True|String||
|Description|Specify description of the new object.|False|String||



##### JSON Results
```json
{"object_code": "attack_pattern", "description": "New Attack Pattern", "created_at": "2020-08-05 13:25:37", "updated_at": "2020-08-05 13:25:37", "object_id": 6, "object_name": "Attack Pattern", "value": "1111", "object_name_plural": "Attack Patterns", "id": 4}
```



#### Enrich Email
Enrich an email address using ThreatQ information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Score Threshold|Set the acceptable score threshold for the entity. If the score exceeds the specified threshold, entity will be marked as suspicious.|False|String|5|
|Show Sources|If enabled, action will return an additional table with related sources.|False|Boolean|true|
|Show Comments|If enabled, action will return an additional table with related comments.|False|Boolean|true|
|Show Attributes|If enabled, action will return an additional table with related attributes.|False|Boolean|true|
|Mark Whitelisted Entities As Suspicious|If enabled, action will mark entities as suspicious if they passed the allowed threshold, even if the entity is whitelisted in ThreatQ.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"status": {"description": "No longer poses a serious threat.", "name": "Expired", "id": 2}, "hash": "f74ee458b6e12452a04c6595bb3cd2d9", "adversaries": [], "status_id": 2, "created_at": "2020-04-15 13:37:43", "type_id": 5, "updated_at": "2020-04-15 13:37:43", "value": "star@star.star", "id": 36, "touched_at": "2020-04-15 13:37:43", "sources": [{"name": "Domain Tools", "source_type": "plugins", "creator_source_id": 8, "created_at": "2020-04-15 13:37:43", "indicator_type_id": 5, "updated_at": "2020-04-15 13:37:43", "indicator_status_id": 2, "indicator_id": 36, "published_at": "2020-04-15 13:37:43", "reference_id": 1, "source_id": 5, "id": 44}], "published_at": "2020-04-15 13:37:43", "score": 0, "type": {"class": "network", "name": "Email Address", "id": 5}, "class": "network", "expired_at": "2020-04-15 13:37:43"}]}, "Entity": "email@example.com"}]
```



#### Get Indicator Details
Search for entities in ThreatQ and get detailed information.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"signatures": [], "attachments": [], "type_id": 30, "expires_needs_calc": "N", "updated_at": "2020-03-15 15:51:13", "touched_at": "2020-03-15 15:51:13", "sources": [{"name": "Emerging Threats", "created_at": "2020-03-15 15:49:04", "updated_at": "2020-03-15 15:49:04", "published_at": null, "reference_id": 2, "pivot": {"source_id": 6, "indicator_id": 7, "id": 9, "creator_source_id": 8}, "type": "plugins", "id": 6, "tlp_id": null}], "id": 7, "last_detected_at": null, "comments": [], "score": {"created_at": "2020-03-15 15:49:04", "updated_at": "2020-03-15 15:49:04", "generated_score": "0.00", "indicator_id": 7, "score_config_hash": "7f8b888a2d2b462310d5227aa75e8c4a78973a96", "manual_score": null}, "indicators": [], "type": {"wildcard_matching": "Y", "name": "URL", "created_at": "2020-01-23 20:08:09", "updated_at": "2020-01-23 20:08:09", "id": 30, "score": null, "plugins": [{"description": "Enrichment data made available by virustotal.com", "package_name": "tq-op-virustotal", "author": "ThreatQ", "disable_proxy": 0, "enabled": 1, "created_at": "2020-01-23 20:09:36", "friendly_name": "VirusTotal", "updated_at": "2020-03-11 12:00:15", "version": "0.0.2", "object_type_id": 30, "config": [{"user_editable": 1, "created_at": "2020-01-23 20:09:46", "mask": true, "updated_at": "2020-03-11 12:02:00", "value": "e4333fb7d82dd5e2040b5e34265094dcc5eeb88141fffc97401ca11282d1a23e", "options": null, "key": "api_key", "plugin_id": 3, "type": "password", "id": 3}], "deleted_at": null, "logo_path": "VirusTotal.png", "id": 3, "required_threatq_version": "2.1", "name": "virustotal"}], "class": "network"}, "events": [], "status": {"user_editable": "N", "created_at": "2020-01-23 20:09:19", "updated_at": "2020-01-23 20:09:19", "name": "Active", "visible": "Y", "protected": "Y", "include_in_export": "Y", "id": 1, "description": "Poses a threat and is being exported to detection tools."}, "hash": "69d4269b838ce143e6f0656384c58f00", "description": "<p>URL</p>", "adversaries": [], "status_id": 1, "expires_at": null, "class": "network", "expired_at": null, "created_at": "2020-03-15 15:49:04", "value": "www.example.com", "expires_calculated_at": "2020-03-15 15:55:01", "watchlist": [], "attributes": [{"name": "Category", "sources": [{"name": "Domain Tools", "created_at": "2020-03-15 15:51:03", "updated_at": "2020-03-15 15:51:03", "published_at": null, "reference_id": 1, "pivot": {"source_id": 5, "creator_source_id": 8, "indicator_attribute_id": 5, "id": 5}, "type": "plugins", "id": 5, "tlp_id": null}], "attribute": {"updated_at": "2020-01-23 20:08:15", "created_at": "2020-01-23 20:08:15", "id": 1, "name": "Category"}, "created_at": "2020-03-15 15:51:03", "updated_at": "2020-03-15 15:51:03", "value": "Malware", "touched_at": "2020-03-15 15:51:03", "indicator_id": 7, "attribute_id": 1, "id": 5}]}, "Entity": "www.example.com"}]
```



#### Enrich URL
Enrich an URL using ThreatQ information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Score Threshold|Set the acceptable score threshold for the entity. If the score exceeds the specified threshold, entity will be marked as suspicious.|False|String|5|
|Show Sources|If enabled, action will return an additional table with related sources.|False|Boolean|true|
|Show Comments|If enabled, action will return an additional table with related comments.|False|Boolean|true|
|Show Attributes|If enabled, action will return an additional table with related attributes.|False|Boolean|true|
|Mark Whitelisted Entities As Suspicious|If enabled, action will mark entities as suspicious if they passed the allowed threshold, even if the entity is whitelisted in ThreatQ.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"status": {"description": "Poses a threat and is being exported to detection tools.", "name": "Active", "id": 1}, "hash": "e216253c1198b44c99c6841899c68418", "adversaries": [], "status_id": 1, "created_at": "2020-04-08 08:59:59", "type_id": 30, "updated_at": "2020-04-08 08:59:59", "value": "example2.sk", "id": 19, "touched_at": "2020-04-08 08:59:59", "sources": [{"name": "tip.labops@siemplify.co", "source_type": "users", "creator_source_id": 8, "created_at": "2020-04-08 08:59:59", "indicator_type_id": 30, "updated_at": "2020-04-08 08:59:59", "indicator_status_id": 1, "indicator_id": 19, "published_at": "2020-04-08 08:59:59", "reference_id": 1, "source_id": 8, "id": 21}], "published_at": "2020-04-08 08:59:59", "score": 0, "expires_calculated_at": "2020-04-08 09:00:01", "type": {"class": "network", "name": "URL", "id": 30}, "class": "network"}]}, "Entity": "example2.sk"}, {"EntityResult": {"total": 1, "data": [{"status": {"description": "Poses a threat and is being exported to detection tools.", "name": "Active", "id": 1}, "hash": "69d4269b838ce143e6f0656384c58ff8", "description": "<p>URL</p>", "adversaries": [], "status_id": 1, "created_at": "2020-03-15 15:49:04", "tags": ["URL"], "updated_at": "2020-03-15 15:51:13", "value": "www.example.com", "id": 7, "touched_at": "2020-03-15 15:51:13", "sources": [{"name": "Emerging Threats", "source_type": "plugins", "creator_source_id": 8, "created_at": "2020-03-15 15:49:04", "indicator_type_id": 30, "updated_at": "2020-03-15 15:49:04", "indicator_status_id": 1, "indicator_id": 7, "published_at": "2020-03-15 15:49:04", "reference_id": 2, "source_id": 6, "id": 9}], "published_at": "2020-03-15 15:49:04", "score": 0, "expires_calculated_at": "2020-03-15 15:50:02", "type_id": 30, "attributes": [{"name": "Category", "created_at": "2020-03-15 15:51:03", "updated_at": "2020-03-15 15:51:03", "value": "Malware", "touched_at": "2020-03-15 15:51:03", "indicator_id": 7, "attribute_id": 1, "id": 5}], "type": {"class": "network", "name": "URL", "id": 30}, "class": "network"}]}, "Entity": "www.example.com"}]
```



#### Enrich Hash
Enrich a Hash using ThreatQ information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Score Threshold|Set the acceptable score threshold for the entity. If the score exceeds the specified threshold, entity will be marked as suspicious.|False|String|5|
|Show Sources|If enabled, action will return an additional table with related sources.|False|Boolean|true|
|Show Comments|If enabled, action will return an additional table with related comments.|False|Boolean|true|
|Show Attributes|If enabled, action will return an additional table with related attributes.|False|Boolean|true|
|Mark Whitelisted Entities As Suspicious|If enabled, action will mark entities as suspicious if they passed the allowed threshold, even if the entity is whitelisted in ThreatQ.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"status": {"description": "Poses a threat and is being exported to detection tools.", "name": "Active", "id": 1}, "hash": "8b168f614b40150266d304dbd5c78036", "adversaries": [], "status_id": 1, "created_at": "2020-03-11 11:26:32", "tags": ["malware", "trojan"], "updated_at": "2020-04-07 13:08:42", "value": "d41d8cd98f00b204e9800998ecf8427e", "id": 2, "touched_at": "2020-04-07 13:08:42", "sources": [{"name": "Domain Tools", "source_type": "plugins", "creator_source_id": 8, "created_at": "2020-03-15 15:04:31", "indicator_type_id": 18, "updated_at": "2020-03-15 15:04:31", "indicator_status_id": 1, "indicator_id": 2, "published_at": "2020-03-15 15:04:31", "reference_id": 1, "source_id": 5, "id": 7}, {"name": "tip.labops@siemplify.co", "source_type": "users", "creator_source_id": 8, "created_at": "2020-03-11 11:26:32", "indicator_type_id": 18, "updated_at": "2020-03-11 12:25:17", "indicator_status_id": 1, "indicator_id": 2, "published_at": "2020-03-11 11:26:32", "reference_id": 1, "source_id": 8, "id": 2}], "published_at": "2020-03-11 11:26:32", "score": 10, "comments": [{"source_name": "tip.labops@siemplify.co", "creator_source_id": 8, "created_at": "2020-03-11 12:32:22", "updated_at": "2020-03-11 12:32:22", "value": "Comment", "indicator_id": 2, "id": 1}], "type_id": 18, "attributes": [{"name": "Category", "created_at": "2020-03-11 11:28:58", "updated_at": "2020-03-11 11:28:58", "value": "Malware", "touched_at": "2020-03-11 11:28:58", "indicator_id": 2, "attribute_id": 1, "id": 1}, {"name": "VirusTotal: Permalink", "created_at": "2020-03-11 12:34:47", "updated_at": "2020-03-11 12:34:47", "value": "https://www.virustotal.com/file/e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855/analysis/1583929494/", "touched_at": "2020-03-11 12:34:47", "indicator_id": 2, "attribute_id": 3, "id": 2}], "type": {"class": "host", "name": "MD5", "id": 18}, "class": "host"}]}, "Entity": "d41d8cd98f00b204e9800998ecf8427e"}, {"EntityResult": {"total": 1, "data": [{"status": {"description": "No longer poses a serious threat.", "name": "Expired", "id": 2}, "hash": "4ca64ed42f6f4e49f1775e5c63d371cd", "description": "<p>Test&nbsp;ד מונחים מועמדים של, דת דפים מאמרשיחהצפה זא</p>", "adversaries": [], "status_id": 2, "created_at": "2020-04-08 12:47:35", "type_id": 23, "updated_at": "2020-04-09 08:00:35", "value": "8e545e1c31f91f777c894b3bd2c2e7d7044cc9dd", "id": 25, "touched_at": "2020-04-09 08:01:42", "sources": [{"name": "Investigation1", "source_type": "other_sources", "creator_source_id": 8, "created_at": "2020-04-08 12:47:35", "indicator_type_id": 23, "updated_at": "2020-04-08 12:47:35", "indicator_status_id": 2, "indicator_id": 25, "published_at": "2020-04-08 12:47:35", "reference_id": 1, "source_id": 9, "id": 27}, {"name": "דת דפים מאמרשיחהצפ", "source_type": "other_sources", "creator_source_id": 8, "created_at": "2020-04-09 08:01:42", "indicator_type_id": 23, "updated_at": "2020-04-09 08:01:42", "indicator_status_id": 2, "indicator_id": 25, "published_at": "2020-04-09 08:01:42", "reference_id": 2, "source_id": 10, "id": 32}], "published_at": "2020-04-08 12:47:35", "score": 0, "type": {"class": "host", "name": "SHA-1", "id": 23}, "class": "host", "expired_at": "2020-04-08 12:47:35"}]}, "Entity": "8e545e1c31f91f777c894b3bd2c2e7d7044cc9dd"}]
```



#### Enrich IP
Enrich an IP using ThreatQ information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Score Threshold|Set the acceptable score threshold for the entity. If the score exceeds the specified threshold, entity will be marked as suspicious.|False|String|5|
|Show Sources|If enabled, action will return an additional table with related sources.|False|Boolean|true|
|Show Comments|If enabled, action will return an additional table with related comments.|False|Boolean|true|
|Show Attributes|If enabled, action will return an additional table with related attributes.|False|Boolean|true|
|Mark Whitelisted Entities As Suspicious|If enabled, action will mark entities as suspicious if they passed the allowed threshold, even if the entity is whitelisted in ThreatQ.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"status": {"description": "No longer poses a serious threat.", "name": "Expired", "id": 2}, "hash": "cb8036b0a7a0ebeeff97a5fe620c4b2c", "description": "<p>דת דפים מאמרשיחהצפ</p>", "adversaries": [], "status_id": 2, "created_at": "2020-04-08 13:09:02", "type_id": 15, "updated_at": "2020-04-09 08:46:43", "value": "8.8.8.8", "id": 27, "touched_at": "2020-04-09 08:46:50", "sources": [{"name": "דת דפים מאמרשיחהצפ", "source_type": "other_sources", "creator_source_id": 8, "created_at": "2020-04-08 13:09:02", "indicator_type_id": 15, "updated_at": "2020-04-08 13:10:11", "indicator_status_id": 2, "indicator_id": 27, "published_at": "2020-04-08 13:09:02", "reference_id": 2, "source_id": 10, "id": 30}], "published_at": "2020-04-08 13:09:02", "score": 0, "comments": [{"source_name": "example@mail.com", "creator_source_id": 8, "created_at": "2020-04-09 08:46:50", "updated_at": "2020-04-09 08:46:50", "value": "דת דפים מאמרשיחהצפawdwqwq", "indicator_id": 27, "id": 5}], "attributes": [{"name": "דת דפים מאמרשיחהצפ", "created_at": "2020-04-09 08:46:26", "updated_at": "2020-04-09 08:46:26", "value": "hvvhv", "touched_at": "2020-04-09 08:46:26", "indicator_id": 27, "attribute_id": 4, "id": 6}], "type": {"class": "network", "name": "IP Address", "id": 15}, "class": "network", "expired_at": "2020-04-08 13:10:11"}]}, "Entity": "8.8.8.8"}]
```



#### Create Adversary
Create an adversary in ThreatQ.
Timeout - 600 Seconds



##### JSON Results
```json
{"tip1@siemplify.com": {"updated_at": "2020-07-30 09:48:36", "created_at": "2020-07-30 09:48:36", "id": 19, "name": "tip1@siemplify.com"}, "tip2@siemplify.com": {"updated_at": "2020-07-30 09:48:36", "created_at": "2020-07-30 09:48:36", "id": 20, "name": "tip2@siemplify.com"}}
```



#### Get Malware Details
Action returns information about malware based on entities from ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Additional Information|Specify what additional fields should be included in the response. Possible values: adversaries, attackPattern, campaign, courseOfAction, attachments, attributes, comments, events, indicators, signatures, sources, status, tags, type, watchlist, exploitTarget, identity, incident, intrusionSet, malware, report, tool, ttp, vulnerability, tasks|False|String|adversaries,attackPattern,campaign,courseOfAction,attachments,attributes,comments,events,indicators,signatures,sources,status,tags,type,watchlist,exploitTarget,identity,incident,intrusionSet,malware,report,tool,ttp,vulnerability,tasks|



##### JSON Results
```json
[{"EntityResult": {"intrusion_set": [], "signatures": [], "object_code": "malware", "attachments": [], "campaign": [], "type_id": null, "ttp": [], "updated_at": "2020-07-08 15:59:20", "touched_at": "2020-08-07 04:55:26", "sources": [{"name": "Domain Tools", "created_at": "2020-07-08 15:59:20", "updated_at": "2020-07-08 15:59:20", "published_at": null, "reference_id": 1, "pivot": {"source_id": 5, "creator_source_id": 8, "malware_id": 1, "id": 1}, "type": "plugins", "id": 5, "tlp_id": null}], "tasks": [{"description": "<p>Task2</p>\n", "status_id": 1, "due_at": null, "creator_source_id": 8, "created_at": "2020-07-09 06:25:54", "updated_at": "2020-07-09 06:25:54", "priority": "Low", "completed_at": null, "assigned_at": "2020-07-09 06:25:54", "assignee_source_id": 8, "pivot": {"created_at": "2020-07-09 06:25:55", "id": 9, "updated_at": "2020-07-09 06:25:55"}, "id": 5, "name": "Task2"}], "object_id": 9, "id": 1, "malware": [{"object_code": "malware", "description": "Koko", "type_id": null, "created_at": "2020-07-21 08:42:09", "status_id": null, "updated_at": "2020-07-21 08:42:09", "value": "Adversary Nameaaa", "touched_at": "2020-08-07 07:35:24", "object_name": "Malware", "object_id": 9, "pivot": {"created_at": "2020-08-07 04:55:26", "id": 69, "updated_at": "2020-08-07 04:55:26"}, "object_name_plural": "Malware", "id": 2}], "object_name_plural": "Malware", "tags": [], "comments": [], "object_name": "Malware", "indicators": [], "type": null, "events": [], "status": null, "description": "<p>Investigation1</p>\n", "adversaries": [{"name": "Tatjana test 1", "created_at": "2020-08-05 06:00:03", "updated_at": "2020-08-05 06:00:03", "touched_at": "2020-08-06 09:03:49", "pivot": {"created_at": "2020-08-06 08:04:58", "id": 51, "updated_at": "2020-08-06 08:04:58"}, "id": 29}], "status_id": null, "tool": [], "exploit_target": [], "incident": [], "report": [], "identity": [], "attack_pattern": [], "created_at": "2020-07-08 15:59:20", "vulnerability": [], "value": "Investigation1", "watchlist": [], "attributes": [], "course_of_action": []}, "Entity": "Investigation1"}]
```



#### Link Entities To Object
Action links all of the entities in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|Specify the type of the object to which you want to link entities.|True|List|Adversary|
|Object Identifier|Specify identifier of the object to which you want to link entities. For example, it can be an MD5 hash, title of the event, name of the adversary etc.|True|String||
|Indicator Type|Specify the type of the  indicator to which you want to link entities. This parameter is only used, if Source Object Type is “Indicator”.|False|List|ASN|



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"last_detected_at": null, "hash": "36c90140xxxe9719de547b8c3616e1a7", "description": null, "status_id": 1, "created_at": "2020-08-18 15:14:15", "type_id": 26, "expires_needs_calc": "N", "updated_at": "2020-08-18 15:25:50", "value": "e54ee7e285fbb0275279143abc4c554e5314e7b417ecac83a5984a964facbaad68866a2841c3e83ddf125a2985566261c4014f9f960xxx0253aebcda9513a9b4", "id": 2196, "touched_at": "2020-08-20 08:20:24", "expires_calculated_at": "2020-08-20 08:25:02", "expires_at": null, "pivot": {"created_at": "2020-08-19 14:46:55", "id": 9597, "updated_at": "2020-08-19 14:46:55"}, "class": "host", "expired_at": null}]}, "Entity": "e54ee7e285fbb0275279143abc4c554e5314e7b417ecac83a5984a964facbaad68866a2841c3e83ddf125a2985566261c4014f9f960ec6xxx3aebcda9513a9b4"}, {"EntityResult": {"total": 1, "data": [{"last_detected_at": null, "hash": "87a765664c58e2cxxx82f6af42319b0f", "description": null, "status_id": 1, "created_at": "2020-08-13 16:53:00", "type_id": 18, "expires_needs_calc": "N", "updated_at": "2020-08-19 13:02:56", "value": "06xxx00cc318cd02ed1394c8c54a00e6", "id": 90, "touched_at": "2020-08-19 14:46:59", "expires_calculated_at": "2020-08-19 14:50:02", "expires_at": null, "pivot": {"created_at": "2020-08-19 14:46:52", "id": 9593, "updated_at": "2020-08-19 14:46:52"}, "class": "host", "expired_at": null}]}, "Entity": "06ff900cc318cd02ed1394c8c54a0xxx"}]
```



#### Link Objects
Action links two objects in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source Object Type|Specify the type of the source object.|True|List|Adversary|
|Source Object Identifier|Specify identifier of the source object. For example, it can be an MD5 hash, title of the event, name of the adversary etc.|True|String||
|Source Indicator Type|Specify the type of the source indicator. This parameter is only used, if Source Object Type is Indicator.|False|List||
|Destination Object Type|Specify the type of the destination object.|True|List|Adversary|
|Destination Object Identifier|Specify identifier of the destination object. For example, it can be an MD5 hash, title of the event, name of the adversary etc.|True|String||
|Destination Indicator Type|Specify the type of the destination indicator. This parameter is only used, if Destination Object Type is Indicator.|False|List||



##### JSON Results
```json
{"id":2,"value":"123123","status_id":null,"type_id":null,"description":null,"started_at":"2020-07-20 12:27:00","ended_at":"2020-07-20 12:27:00","created_at":"2020-07-20 12:27:10","updated_at":"2020-07-20 12:27:10","touched_at":"2020-07-20 14:50:14","object_id":4,"object_code":"incident","object_name":"Incident","object_name_plural":"Incidents","pivot":{"id":18,"created_at":"2020-07-20 14:50:14","updated_at":"2020-07-20 14:50:14"}}
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Update Indicator Status
Action updates indicator status in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|Specify the new status of the indicator.|True|List|Active|



##### JSON Results
```json
[{"EntityResult": {"data": {"last_detected_at": null, "hash": "7565b7106768b56356217bfc5e951xxx", "description": null, "status_id": 5, "created_at": "2020-07-30 11:17:42", "type_id": 5, "expires_needs_calc": "N", "updated_at": "2020-08-17 12:36:32", "value": "admin@email.com", "id": 57, "touched_at": "2020-08-17 12:36:32", "expires_calculated_at": null, "expires_at": null, "class": "network", "expired_at": null}}, "Entity": "employee@mail.com"}, {"EntityResult": {"data": {"last_detected_at": null, "hash": "422ef7e72299386a772fb58bf0d86xxx", "description": "EMAIL ADDRESS ACTIVE", "status_id": 5, "created_at": "2020-07-30 11:17:43", "type_id": 5, "expires_needs_calc": "N", "updated_at": "2020-08-17 12:36:29", "value": "attacker@mail.com", "id": 58, "touched_at": "2020-08-17 12:36:29", "expires_calculated_at": "2020-07-30 11:20:02", "expires_at": null, "class": "network", "expired_at": null}}, "Entity": "attacker@mail.com"}, {"EntityResult": {"data": {"last_detected_at": null, "hash": "2ae70ffb3fbc65b0462d8ee8ea1c2xxx", "description": "EMAIL SUBJECT", "status_id": 5, "created_at": "2020-07-30 11:19:10", "type_id": 7, "expires_needs_calc": "N", "updated_at": "2020-08-17 12:36:30", "value": "HTTP://example.com", "id": 60, "touched_at": "2020-08-17 12:36:30", "expires_calculated_at": "2020-08-13 18:00:02", "expires_at": null, "class": "network", "expired_at": null}}, "Entity": "HTTP://example.com"}, {"EntityResult": {"data": {"last_detected_at": null, "hash": "65e668a0d327a7d4cb4550d83b002xxx", "description": "EMAIL SUBJECT", "status_id": 5, "created_at": "2020-07-30 11:19:12", "type_id": 7, "expires_needs_calc": "N", "updated_at": "2020-08-17 12:36:34", "value": "YOUR NEW SALARY NOTIFICATION", "id": 63, "touched_at": "2020-08-17 12:36:34", "expires_calculated_at": "2020-08-06 05:15:03", "expires_at": null, "class": "network", "expired_at": null}}, "Entity": "YOUR NEW SALARY NOTIFICATION"}, {"EntityResult": {"data": {"last_detected_at": null, "hash": "65b9aa337a73fa71b88bd613c1f4dxxx", "description": null, "status_id": 5, "created_at": "2020-07-19 09:17:43", "type_id": 18, "expires_needs_calc": "N", "updated_at": "2020-08-17 12:36:36", "value": "7815696ecbf1c96e6894b779456d3xxx", "id": 2, "touched_at": "2020-08-17 12:36:36", "expires_calculated_at": "2020-08-17 12:00:02", "expires_at": null, "class": "host", "expired_at": null}}, "Entity": "7815696ecbf1c96e6894b779456d3xxx"}]
```



#### List Events
List events from ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Additional Fields|Specify what additional fields should be included in the response. Possible values: adversaries, attachments, attributes, comments, events, indicators, signatures, sources, spearphish, tags, type, watchlist.|False|String|adversaries, attachments, attributes, comments, events, indicators, signatures, sources, spearphish, tags, type, watchlist|
|Sort Field|Specify what field should be used for sorting events.|False|List|ID|
|Sort Direction|Specify the sorting direction.|False|List|Ascending|
|Max Events To Return|Specify how many events to return.|False|String|50|



##### JSON Results
```json
[  {    "created_at": "2020-07-19 09:19:39",    "description": "<p>Test</p>",    "happened_at": "2020-07-19 09:19:00",    "hash": "78f58dacd9c215003911a09d5b3exxxx",    "id": 1,    "title": "Test",    "touched_at": "2020-08-10 09:48:50",    "type_id": 4,    "updated_at": "2020-08-07 23:56:55"  },  {    "created_at": "2020-07-19 09:19:39",    "description": "<p>Test2</p>",    "happened_at": "2020-07-19 09:19:00",    "hash": "78f58dacd9c215003911a09d5b3exxxx",    "id": 2,    "title": "Test2",    "touched_at": "2020-08-10 09:48:50",    "type_id": 4,    "updated_at": "2020-08-07 23:56:55"  },  {    "created_at": "2020-07-19 09:19:39",    "description": "<p>Test3</p>",    "happened_at": "2020-07-19 09:19:00",    "hash": "78f58dacd9c215003911a09d5b3exxxx",    "id": 3,    "title": "Test3",    "touched_at": "2020-08-10 09:48:50",    "type_id": 4,    "updated_at": "2020-08-07 23:56:55"  }]
```



#### Create Event
Create an event in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event Type|Specify the type of the event.|True|List|Spearphish|
|Title|Specify the title of the event.|True|String||
|Happened At|Specify when the event happened. If nothing is entered in this field, action will use current time. Format: YYYY-MM-DD hh:mm:ss|False|String||



##### JSON Results
```json
{"data": {"hash": "5d1ee5105448a27443f8b451c5b081e1", "title": "123123", "created_at": "2020-08-14 11:30:05", "type_id": 1, "updated_at": "2020-08-14 11:30:05", "touched_at": "2020-08-14 11:30:05", "happened_at": "2020-08-14 11:30:02", "type": {"updated_at": "2020-06-29 17:13:28", "user_editable": "N", "created_at": "2020-06-29 17:13:28", "id": 1, "name": "Spearphish"}, "id": 55}}
```



#### List Entity Related Objects
Action lists related objects for entities in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Related Object Type|Specify the type of the related object that needs to be returned.|True|List|Adversary|
|Max Related Objects To Return|Specify how many related objects to return. Maximum is 1000. This is a ThreatQ limitation.|False|String|50|



##### JSON Results
```json
[{"EntityResult": [{"hash": "65e668a0d327a7d4cb4550d83b002d19", "description": "EMAIL SUBJECT", "status_id": 1, "class": "network", "expires_needs_calc": "N", "updated_at": "2020-07-30 11:19:12", "expires_at": null, "touched_at": "2020-08-06 05:10:29", "deleted_at": null, "id": 63, "expired_at": null, "last_detected_at": null, "created_at": "2020-07-30 11:19:12", "type_id": 7, "value": "YOUR NEW SALARY NOTIFICATION", "sync_hash": "a1f45026a8481036d81b5c4479115485", "expires_calculated_at": "2020-08-06 05:15:03"}], "Entity": "CVE-2012-0217"}, {"EntityResult": [{"hash": "0b0d0e4d656cfe05e95fd6cbe95fd6cb", "description": "ghfcv", "status_id": 4, "class": "network", "expires_needs_calc": "N", "updated_at": "2020-08-03 06:13:02", "expires_at": null, "touched_at": "2020-08-06 05:33:22", "deleted_at": null, "id": 84, "expired_at": null, "last_detected_at": null, "created_at": "2020-08-03 06:13:02", "type_id": 32, "value": "8.8.85.5", "sync_hash": "aca1e5b10657c8a3266bb9502b5c05b1", "expires_calculated_at": "2020-08-06 05:35:02"}, {"hash": "de06fc6f5a8192be43d82a6c43d82a6c", "description": "this is string", "status_id": 3, "class": "network", "expires_needs_calc": "N", "updated_at": "2020-08-03 05:58:57", "expires_at": null, "touched_at": "2020-08-06 09:03:48", "deleted_at": null, "id": 82, "expired_at": null, "last_detected_at": null, "created_at": "2020-08-03 05:58:57", "type_id": 27, "value": "testtest", "sync_hash": "0ec37d9eb46538335fcf47c72c774406", "expires_calculated_at": "2020-08-06 09:05:02"}], "Entity": "333.33.33.333"}, {"EntityResult": [{"hash": "c2107c21f7a6f030e3430829cfb3a3d5", "description": null, "status_id": 5, "class": "host", "expires_needs_calc": "N", "updated_at": "2020-07-30 12:21:15", "expires_at": null, "touched_at": "2020-08-06 05:10:29", "deleted_at": null, "id": 66, "expired_at": null, "last_detected_at": null, "created_at": "2020-07-30 12:21:15", "type_id": 4, "value": "CVE-2012-0217", "sync_hash": "e527d6d667b0ab8cc731dadc47c45d8e", "expires_calculated_at": null}], "Entity": "YOUR NEW SALARY NOTIFICATION"}, {"EntityResult": [{"hash": "eb1b619f317518481183980adcbeae95", "description": null, "status_id": 2, "class": "network", "expires_needs_calc": "N", "updated_at": "2020-07-30 12:23:45", "expires_at": null, "touched_at": "2020-08-06 05:09:37", "deleted_at": null, "id": 69, "expired_at": "2020-07-30 12:23:45", "last_detected_at": null, "created_at": "2020-07-30 12:23:45", "type_id": 11, "value": "peterpc.localdomain.local", "sync_hash": "6b5eb36a8c450074a63a740fa1820ece", "expires_calculated_at": null}], "Entity": "c:\\file.txt"}]
```



#### Add Attribute
Action adds an attribute to the object.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|Specify to which object type attribute should be added.|True|List|Adversary|
|Object Identifier|Specify identifier of the object. For example, it can be an MD5 hash, title of the event, name of the adversary etc.|True|String||
|Indicator Type|Specify the type of the indicator. This parameter is only used, if Source Object Type is Indicator.|False|List|ASN|
|Attribute Name|Specify the name of the attribute.|True|String||
|Attribute Value|Specify the value of the attribute.|True|String||
|Attribute Source|Specify the source of the attribute.|False|String||



##### JSON Results
```json
{"name": "Category", "attribute": {"updated_at": "2020-06-29 17:13:35", "created_at": "2020-06-29 17:13:35", "id": 1, "name": "Category"}, "created_at": "2020-08-04 13:06:33", "updated_at": "2020-08-04 13:14:59", "value": "Malware", "sources": [{"name": "tip.labops@siemplify.co", "created_at": "2020-08-04 13:06:33", "updated_at": "2020-08-04 13:14:59", "published_at": null, "reference_id": 1, "pivot": {"source_id": 8, "creator_source_id": 8, "id": 3, "adversary_attribute_id": 3}, "type": "users", "id": 8, "tlp_id": null}], "adversary_id": 15, "attribute_id": 1, "id": 3}
```



#### Enrich CVE
Enrich a CVE using ThreatQ information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Score Threshold|Set the acceptable score threshold for the entity. If the score exceeds the specified threshold, entity will be marked as suspicious.|False|String|5|
|Show Sources|If enabled, action will return an additional table with related sources.|False|Boolean|true|
|Show Comments|If enabled, action will return an additional table with related comments.|False|Boolean|true|
|Show Attributes|If enabled, action will return an additional table with related attributes.|False|Boolean|true|
|Mark Whitelisted Entities As Suspicious|If enabled, action will mark entities as suspicious if they passed the allowed threshold, even if the entity is whitelisted in ThreatQ.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"status": {"description": "Associated to an active indicator or event (i.e. pDNS).", "name": "Indirect", "id": 3}, "hash": "1eb1492a73972823ef9323daec0cbe5c", "description": "<p>asdasd</p>", "adversaries": [], "status_id": 3, "created_at": "2020-03-15 16:03:58", "type_id": 4, "updated_at": "2020-04-09 12:23:27", "value": "CVE-2020-10587", "id": 9, "touched_at": "2020-04-09 12:23:35", "sources": [{"name": "Emerging Threats", "source_type": "plugins", "creator_source_id": 8, "created_at": "2020-03-15 16:03:58", "indicator_type_id": 4, "updated_at": "2020-03-15 16:03:58", "indicator_status_id": 3, "indicator_id": 9, "published_at": "2020-03-15 16:03:58", "reference_id": 2, "source_id": 6, "id": 11}, {"name": "דת דפים מאמרשיחהצפ", "source_type": "other_sources", "creator_source_id": 8, "created_at": "2020-04-09 12:23:35", "indicator_type_id": 4, "updated_at": "2020-04-09 12:23:35", "indicator_status_id": 3, "indicator_id": 9, "published_at": "2020-04-09 12:23:35", "reference_id": 2, "source_id": 10, "id": 39}], "published_at": "2020-03-15 16:03:58", "score": 0, "expires_calculated_at": "2020-03-15 16:05:01", "attributes": [{"name": "דת דפים מאמרשיחהצפ", "created_at": "2020-04-09 12:23:22", "updated_at": "2020-04-09 12:23:22", "value": "hvvhv", "touched_at": "2020-04-09 12:23:22", "indicator_id": 9, "attribute_id": 4, "id": 8}], "type": {"class": "host", "name": "CVE", "id": 4}, "class": "host"}]}, "Entity": "CVE-2020-10587"}]
```



#### Add Source
Action adds a source to the object.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Object Type|Specify to which object type source should be added.|True|List|Adversary|
|Object Identifier|Specify identifier of the object. For example, it can be an MD5 hash, title of the event, name of the adversary etc.|True|String||
|Indicator Type|Specify the type of the indicator. This parameter is only used, if Source Object Type is Indicator.|False|List|ASN|
|Source Name|Specify the name of the source.|True|String||



##### JSON Results
```json
{"name": "123", "creator_source_id": 8, "created_at": "2020-08-05 06:27:51", "updated_at": "2020-08-05 06:27:51", "existing": 0, "published_at": null, "adversary_id": 15, "source_id": 17, "deleted_at": null, "id": 31, "tlp_id": null}
```



#### Create Indicator
Create an indicator in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator Type|Specify the type of the new indicator.|True|List|ASN|
|Status|Specify the status of the new indicator.|True|List|Active|
|Description|Specify description of the new indicator.|False|String||



##### JSON Results
```json
{"tip1@siemplify.com": {"total": 1, "data": [{"last_detected_at": null, "hash": "26ed6f79c7a9d2f666113cc63907071d", "description": "abc", "status_id": 1, "created_at": "2020-07-30 09:43:57", "type_id": 33, "expires_needs_calc": "Y", "updated_at": "2020-07-30 09:43:57", "value": "tip1@siemplify.com", "existing": "N", "touched_at": "2020-07-30 09:43:57", "class": "host", "expires_calculated_at": null, "expires_at": null, "type": {"wildcard_matching": "Y", "name": "Username", "created_at": "2020-06-29 17:13:29", "updated_at": "2020-06-29 17:13:29", "class": "host", "score": null, "id": 33}, "id": 53, "expired_at": null}]}, "tip2@siemplify.com": {"total": 1, "data": [{"last_detected_at": null, "hash": "b68edaa93c823b2c9a7442b31834aecc", "description": "abc", "status_id": 1, "created_at": "2020-07-30 09:43:57", "type_id": 33, "expires_needs_calc": "Y", "updated_at": "2020-07-30 09:43:57", "value": "tip2@siemplify.com", "existing": "N", "touched_at": "2020-07-30 09:43:57", "class": "host", "expires_calculated_at": null, "expires_at": null, "type": {"wildcard_matching": "Y", "name": "Username", "created_at": "2020-06-29 17:13:29", "updated_at": "2020-06-29 17:13:29", "class": "host", "score": null, "id": 33}, "id": 54, "expired_at": null}]}}
```



#### List Related Objects
Action lists related objects in ThreatQ.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source Object Type|Specify the type of the source object.|True|List|Adversary|
|Source Object Identifier|Specify identifier of the source object. For example, it can be an MD5 hash, title of the event, name of the adversary etc.|True|String||
|Source Indicator Type|Specify the type of the source indicator. This parameter is only used, if Source Object Type is Indicator.|False|List||
|Related Object Type|Specify the type of the related object that needs to be returned.|True|List|Adversary|
|Max Related Objects To Return|Specify how many related objects to return.|False|String|50|



##### JSON Results
```json
[{"last_detected_at": null, "hash": "12fc1985a0ab5984cb70385004f32ffa", "description": null, "status_id": 4, "created_at": "2020-07-30 12:25:54", "type_id": 18, "expires_needs_calc": "N", "updated_at": "2020-07-30 12:25:54", "value": "8c71fb3f7593543f2ad180d31148a7cf", "sync_hash": "68430f34910adb87797ca0df95354393", "touched_at": "2020-08-03 07:18:31", "class": "host", "expires_calculated_at": "2020-08-03 07:20:02", "expires_at": null, "pivot": {"src_object_id": 19, "created_at": "2020-08-03 07:18:31", "updated_at": "2020-08-03 07:18:31", "dest_object_id": 71, "src_type": "adversary", "dest_type": "indicator", "id": 28}, "deleted_at": null, "id": 71, "expired_at": null}]
```



#### Link Entities
Action links all of the entities in ThreatQ.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"total": 1, "data": [{"last_detected_at": null, "hash": "36c90140xxxe9719de547b8c3616e1a7", "description": null, "status_id": 1, "created_at": "2020-08-18 15:14:15", "type_id": 26, "expires_needs_calc": "N", "updated_at": "2020-08-18 15:25:50", "value": "e54ee7e285fbb0275279143abc4c554e5314e7b417ecac83a5984a964facbaad68866a2841c3e83ddf125a2985566261c4014f9f960xxx0253aebcda9513a9b4", "id": 2196, "touched_at": "2020-08-20 08:20:24", "expires_calculated_at": "2020-08-20 08:25:02", "expires_at": null, "pivot": {"created_at": "2020-08-19 14:46:55", "id": 9597, "updated_at": "2020-08-19 14:46:55"}, "class": "host", "expired_at": null}]}, "Entity": "e54ee7e285fbb0275279143abc4c554e5314e7b417ecac83a5984a964facbaad68866a2841c3e83ddf125a2985566261c4014f9f960ec6xxx3aebcda9513a9b4"}, {"EntityResult": {"total": 1, "data": [{"last_detected_at": null, "hash": "87a765664c58e2cxxx82f6af42319b0f", "description": null, "status_id": 1, "created_at": "2020-08-13 16:53:00", "type_id": 18, "expires_needs_calc": "N", "updated_at": "2020-08-19 13:02:56", "value": "06xxx00cc318cd02ed1394c8c54a00e6", "id": 90, "touched_at": "2020-08-19 14:46:59", "expires_calculated_at": "2020-08-19 14:50:02", "expires_at": null, "pivot": {"created_at": "2020-08-19 14:46:52", "id": 9593, "updated_at": "2020-08-19 14:46:52"}, "class": "host", "expired_at": null}]}, "Entity": "06ff900cc318cd02ed1394c8c54a0xxx"}]
```









