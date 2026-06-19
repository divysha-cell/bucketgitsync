
# Zendesk

Zendesk Support is a beautifully simple system for tracking, prioritizing, and solving customer support tickets.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|String|https://{username}.zendesk.com|
|User Email Address||True|String||
|Api Token||True|Password|*****|


#### Dependencies
| |
|-|
|certifi-2026.5.20-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.16-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|


## Actions
#### Get Ticket Details
Get ticket details, comments, and attachments by ticket id
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|The ID f the ticket.|True|String|None|



##### JSON Results
```json
{"Details": {"ticket": {"follower_ids": [], "via": {"source": {"to": {}, "from": {}, "rel": "None"}, "channel": "web"}, "updated_at": "2019-02-03T10:08:00Z", "submitter_id": 360638872459, "assignee_id": 360638872459, "brand_id": 360000159559, "id": 2, "custom_fields": [], "satisfaction_rating": "None", "sharing_agreement_ids": [], "allow_attachments": "True", "collaborator_ids": [], "priority": "high", "subject": "Test", "type": "incident", "status": "open", "description": "Test Test Test", "tags": ["test"], "forum_topic_id": "None", "organization_id": 360018882419, "due_at": "None", "is_public": "True", "requester_id": 360638872459, "followup_ids": [], "recipient": "None", "problem_id": "None", "url": "https://xxx.zendesk.com/api/v2/tickets/2.json", "fields": [], "created_at": "2019-02-03T10:08:00Z", "raw_subject": "Test", "email_cc_ids": [], "allow_channelback": "False", "has_incidents": "False", "group_id": 360000361099, "external_id": "None"}}, "Comments": [{"body": "Test Test Test", "plain_body": "Test Test Test", "via": {"source": {"to": {}, "from": {}, "rel": "None"}, "channel": "web"}, "attachments": [{"thumbnails": [], "url": "https://xxx.zendesk.com/api/v2/attachments/360701661660.json", "file_name": "Siemplify 10 2018-12-11 (1).lic", "content_url": "https://xxx.zendesk.com/attachments/token/GeO6Xbc5I009xGRKLwWd7u7Qv/?name=Xxx+10+2018-12-11+%281%29.lic", "height": "None", "width": "None", "mapped_content_url": "https://xxx.zendesk.com/attachments/token/GeO6Xbc5I009xGRKLwWd7u7Qv/?name=Xxx+10+2018-12-11+%281%29.lic", "content_type": "application/unknown", "inline": "False", "id": 360701661660, "size": 1272}], "audit_id": 393260420939, "created_at": "2019-02-03T10:08:00Z", "id": 393260420979, "author_id": 360638872459, "html_body": "<div> Test Test Test < br >< /div>", "type": "Comment", "public": "True", "metadata": {"system": {"latitude": 32.066599999999994, "client": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/71.0.3578.98 Safari/537.36", "ip_address": "1.1.1.1", "location": "Tel Aviv, 05, Israel", "longitude": 34.764999999999986}, "custom": {}}}], "Attachments": [{"test.txt": ""}]}
```



#### Update Ticket
Update existing ticket details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Ticket number.|True|String|None|
|Subject|The subject of the ticket.|False|String|None|
|Assigned User|User full name.|False|String|None|
|Assignment Group|Group name.|False|String|None|
|Priority|Priority will be one of the following: urgent, high, normal or low.|False|String||
|Ticket Type|The ticket type will be one of the following: problem, incident, question or task.|False|String||
|Tag|Tag to add to the ticket.|False|String||
|Status|The status will be one of the following: new, open, pending, hold, solved or closed.|False|String||
|Internal Note|Specify whether the comment should be public, or internal. Unchecked means it will be public, checked means it will be internal only.|False|Boolean|False|
|Additional Comment|If you want to add a comment to the ticket, specify the text you would like to add as a comment here.|False|String||



#### Search Tickets
Search tickets by keyword
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Query|Query content(e.g: type:ticket status:pending).|True|String||



##### JSON Results
```json
{"count": 2, "facets": "None", "previous_page": "None", "next_page": "None", "results": [{"follower_ids": [], "via": {"source": {"to": {}, "from": {}, "rel": "None"}, "channel": "sample_ticket"}, "updated_at": "2019-02-03T10:03:42Z", "submitter_id": 360638872459, "assignee_id": 360638872459, "brand_id": 360000159559, "id": 1, "custom_fields": [], "satisfaction_rating": "None", "sharing_agreement_ids": [], "allow_attachments": "True", "collaborator_ids": [], "priority": "normal", "subject": "Sample ticket: Meet the ticket", "type": "incident", "status": "open", "description": "Hi \\\\u202aTTT,\\n\\nEmails, chats, voicemails, and tweets are captured in Zendesk Support as tickets. Start typing above to respond and click Submit to send. To test how an email becomes a ticket, send a message to support@xxx.zendesk.com.\\n\\nCurious about what your customers will see when you reply? Check out this video:\\nhttps://demos.zendesk.com/hc/en-us/articles/202341799\\n", "tags": ["sample", "support", "zendesk"], "forum_topic_id": "None", "organization_id": "None", "due_at": "None", "is_public": "True", "requester_id": 360641174479, "followup_ids": [], "recipient": "None", "problem_id": "None", "url": "https://xxx.zendesk.com/api/v2/tickets/1.json", "fields": [], "created_at": "2019-02-03T10:03:42Z", "raw_subject": "Sample ticket: Meet the ticket", "email_cc_ids": [], "allow_channelback": "False", "has_incidents": "False", "group_id": 360000361099, "external_id": "None", "result_type": "ticket"}, {"follower_ids": [], "via": {"source": {"to": {}, "from": {}, "rel": "None"}, "channel": "web"}, "problem_i0": "None", "updated_at": "2019-02-03T10:08:00Z", "submitter_id": 360638872459, "assignee_id": 360638872459, "brand_id": 360000159559, "id": 2, "custom_fields": [], "satisfaction_rating": "None", "sharing_agreement_ids": [], "allow_attachments": "True", "collaborator_ids": [], "priority": "high", "subject": "Test", "type": "incident", "status": "open", "description": "Test Test Test", "tags": ["test"], "forum_topic_id": "None", "organization_id": 360018882419, "due_at": "None", "is_public": "True", "requester_id": 360638872459, "followup_ids": [], "recipient": "None", "url": "https://xxx.zendesk.com/api/v2/tickets/2.json", "fields": [], "created_at": "2019-02-03T10:08:00Z", "raw_subject": "Test", "email_cc_ids": [], "allow_channelback": "False", "has_incidents": "False", "group_id": 360000361099, "external_id": "None", "result_type": "ticket"}]}
```



#### Apply Macros On Ticket
Apply macro to a ticket
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Ticket number.|True|String|None|
|Macro Title|Macro Title|True|String|None|



#### Add Comment To Ticket
Add a comment to an existing ticket
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify the Zendesk Ticket ID for which you would like to add a comment.|True|String||
|Comment Body|Provide the text you would like to be contained in the comment body|True|Content||
|Author Name|Specify the name of the author, please make sure this name exists on Zendesk|False|String|None|
|Internal Note|Specify whether the comment should be public, or internal. Unchecked means it will be public, checked means it will be internal only.|False|Boolean||



#### Create Ticket
Create a ticket with specific properties
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Priority|Priority will be one of the following: urgent, high, normal or low.|False|String||
|Ticket Type|The ticket type will be one of the following: problem, incident, question or task.|False|String||
|Subject|Subject|True|String||
|Description|Description|True|String||
|Assigned User|User full name.|False|String||
|Assignment Group|Group name.|False|String||
|Tag|Tag|False|String||
|Internal Note|Specify whether the comment should be public, or internal. Unchecked means it will be public, checked means it will be internal only.|False|Boolean|False|
|Email CCs|Specify a comma-separated list of email addresses, which should also receive the notification of the ticket creation. Note: at max 48 email CCs can be added. This is Zendesk limitation.|False|String||
|Validate Email CCs|If enabled, action will try to check that users with emails provided in “Email CCs“ parameter exist. If at least one user doesn’t exist, action will fail. If this parameter is disabled, action will not perform this check.|False|Boolean|true|



#### Ping
Test Connectivity
Timeout - 600 Seconds









