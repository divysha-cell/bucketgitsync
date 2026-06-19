
# ZohoDesk

Zoho Desk is context-aware customer service software that helps you put your customers at the heart of the company.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Zoho Desk instance.|True|String|https://desk.zoho.{region}|
|Client ID|Client ID of the Zoho Desk account.|True|String||
|Client Secret|Client Secret of the Zoho Desk account.|True|Password|*****|
|Refresh Token|Refresh Token of the Zoho Desk account. You need to run the action "Get Refresh Token" to generate it.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Zoho Desk server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|protobuf-5.28.0-cp38-abi3-manylinux2014_x86_64.whl|
|google_api_python_client-2.143.0-py2.py3-none-any.whl|
|httpcore-1.0.5-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|google_api_core-2.19.2-py3-none-any.whl|
|typing_extensions-4.12.2-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|anyio-4.4.0-py3-none-any.whl|
|pyparsing-3.1.4-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|TIPCommon-2.0.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the Zoho Desk with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Get Refresh Token
Get a refresh token for the configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Authorization Link|Specify the authorization link for the integration.|True|String|https://accounts.zoho.{region}/oauth/v2/token|
|Authorization Code|Specify the authorization code that was generated in the dev console of Zoho.|True|Password|*****|



#### Get Ticket Details
Get detailed information about the ticket from Zoho Desk.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket IDs|Specify a comma-separated list of ids for which you want to return details.|True|String||
|Create Insight|If enabled, action will create an insight containing information about tickets.|False|Boolean|false|
|Additional Fields To Return|Specify what additional fields to return. Possible values: contacts, products, assignee, departments, contract, isRead, team, skills.|False|String|contacts, products, assignee, departments, contract, isRead, team, skills|
|Fetch Comments|If enabled, action will fetch comments related to the tickets.|False|Boolean|true|
|Max Comments To Return|Specify how many comments to return per ticket. Default: 50. Maximum: 100.|False|String|50|



##### JSON Results
```json
[{"modifiedTime":"2022-06-27T17:12:35.000Z","subCategory":null,"statusType":"Open","subject":"tesa","dueDate":null,"departmentId":"97709xxxxxxxxxxx","channel":"Phone","onholdTime":null,"language":null,"source":{"appName":null,"extId":null,"permalink":null,"type":"SYSTEM","appPhotoURL":null},"resolution":null,"sharedDepartments":[],"closedTime":null,"approvalCount":"0","isOverDue":false,"isTrashed":false,"contact":{"firstName":null,"lastName":"test","phone":null,"mobile":null,"id":"97709xxxxxxxxxxxx","isSpam":false,"type":null,"email":"test@test.com","account":{"website":null,"accountName":"test!@test.com","id":"97709xxxxxxxxxxx"}},"createdTime":"2022-06-27T17:12:35.000Z","id":"97709xxxxxxxxxxx","isResponseOverdue":false,"customerResponseTime":"2022-06-27T17:12:35.000Z","productId":null,"contactId":"97709xxxxxxxxxxx","threadCount":"1","secondaryContacts":[],"priority":null,"classification":null,"commentCount":"0","taskCount":"0","accountId":"97709xxxxxxxxxxx","phone":null,"webUrl":"https://desk.zoho.eu/support/siemplify/ShowHomePage.do#Cases/dv/97709xxxxxxxxxxx","assignee":{"photoURL":"https://desk.zoho.eu/api/v1/agents/97709xxxxxxxxxxx/photo?orgId=2008xxxxx","firstName":"TIP","lastName":"Labops","id":"97709xxxxxxxxxxx","email":"tip.labops@siemplify.co"},"isSpam":false,"status":"Open","entitySkills":[],"ticketNumber":"102","sentiment":null,"customFields":{"System Administrator email":null,"Website URL":null,"URL1":null},"isArchived":false,"skillsInfo":[],"isRead":true,"description":"<div style=\"font-size: 13px; font-family: Regular, Lato, Arial, Helvetica, sans-serif\"><div>tetsta</div></div>","timeEntryCount":"0","channelRelatedInfo":null,"responseDueDate":null,"isDeleted":false,"modifiedBy":"97709xxxxxxxxxxx","department":{"name":"Siemplify","id":"97709xxxxxxxxxxx"},"followerCount":"0","email":"test@test.com","layoutDetails":{"id":"97709xxxxxxxxxxx","layoutName":"Siemplify"},"channelCode":null,"product":null,"isFollowing":false,"cf":{"cf_url":null,"cf_website_url":null,"cf_system_administrator_email":null},"slaId":null,"team":null,"layoutId":"97709xxxxxxxxxxx","assigneeId":"97709xxxxxxxxxxx","createdBy":"97709xxxxxxxxxxx","teamId":null,"contractId":null,"tagCount":"0","attachmentCount":"0","isEscalated":false,"category":null,"comments":[]},{"modifiedTime":"2022-07-06T07:48:08.000Z","subCategory":"ewq","statusType":"Open","subject":"Here's your first ticket.","dueDate":"2022-07-06T07:05:43.000Z","departmentId":"97709xxxxxxxxxxx","channel":"Chat","onholdTime":null,"language":"English","source":{"appName":null,"extId":null,"permalink":null,"type":"SYSTEM","appPhotoURL":null},"resolution":"Koko","sharedDepartments":[],"closedTime":null,"approvalCount":"0","isOverDue":true,"isTrashed":false,"contact":{"firstName":null,"lastName":"Lawrence","phone":"1 888 xxx xxxx","mobile":null,"id":"97709xxxxxxxxxxx","isSpam":false,"type":null,"email":"support@zohosupport.com","account":{"website":"https://www.zoho.com/","accountName":"Zoho","id":"97709xxxxxxxxxxx"}},"createdTime":"2022-06-27T17:02:17.000Z","id":"97709xxxxxxxxxxx","isResponseOverdue":false,"customerResponseTime":"2022-06-27T17:02:17.000Z","productId":null,"contactId":"97709xxxxxxxxxxx","threadCount":"1","secondaryContacts":[],"priority":null,"classification":null,"commentCount":"2","taskCount":"0","accountId":"97709xxxxxxxxxxx","phone":"1 888 xxx xxxx","webUrl":"https://desk.zoho.eu/support/siemplify/ShowHomePage.do#Cases/dv/97709xxxxxxxxxxx","assignee":null,"isSpam":false,"status":"Open","entitySkills":[],"ticketNumber":"101","sentiment":null,"customFields":{"System Administrator email":null,"Website URL":null,"URL1":null},"isArchived":false,"skillsInfo":[],"isRead":true,"description":"Hello<br /><br />Welcome to Zoho Desks new Unified Ticket Screen. Here, you have complete context of the ticket. Now that you had received your first ticket, did you notice that it has been assigned to you? To respond to this ticket smartly, check out the Auto-Suggested Solutions in the pane to your left.<br /><br />When you're done composing your response, you may send it and close the ticket.<br /><br />Whatever action you perform, be rest assured that you can always track them under the ticket's history. With that, you're one step closer to delivering top-notch customer service!<br /><br />Cheers,<br />Team Zoho Desk<br />1 888 xxx xxxx","timeEntryCount":"0","channelRelatedInfo":null,"responseDueDate":null,"isDeleted":false,"modifiedBy":"97709xxxxxxxxxxx","department":{"name":"Siemplify","id":"97709xxxxxxxxxxx"},"followerCount":"0","email":"support@zohosupport.com","layoutDetails":{"id":"97709xxxxxxxxxxx","layoutName":"Siemplify"},"channelCode":null,"product":null,"isFollowing":false,"cf":{"cf_url":null,"cf_website_url":null,"cf_system_administrator_email":null},"slaId":null,"team":{"name":"koko","id":"97709xxxxxxxxxxx"},"layoutId":"97709xxxxxxxxxxx","assigneeId":null,"createdBy":"97709xxxxxxxxxxx","teamId":"97709xxxxxxxxxxx","contractId":null,"tagCount":"1","attachmentCount":"0","isEscalated":false,"category":"qwe","comments":[{"content":"<div style=\"font-size: 14px; font-family: LatoRegular, Regular, Lato, &quot;Lato 2&quot;, Arial, Helvetica, sans-serif\"><div style=\"font-size: 14px; font-family: LatoRegular, Regular, Lato, &quot;Lato 2&quot;, Arial, Helvetica, sans-serif\"><ul><li>asdasdasdasd<br /></li></ul></div><div><br /></div></div>","commentedTime":"2022-06-29T10:21:24.000Z","modifiedTime":"2022-06-29T10:23:42.000Z","contentType":"html","impersonatedUser":null,"encodedContent":"&lt;div style&#x3d;&quot;font-size&#x3a; 14px&#x3b; font-family&#x3a; LatoRegular, Regular, Lato, &amp;quot&#x3b;Lato 2&amp;quot&#x3b;, Arial, Helvetica, sans-serif&quot;&gt;&lt;div style&#x3d;&quot;font-size&#x3a; 14px&#x3b; font-family&#x3a; LatoRegular, Regular, Lato, &amp;quot&#x3b;Lato 2&amp;quot&#x3b;, Arial, Helvetica, sans-serif&quot;&gt;&lt;ul&gt;&lt;li&gt;asdasdasdasd&lt;br &#x2f;&gt;&lt;&#x2f;li&gt;&lt;&#x2f;ul&gt;&lt;&#x2f;div&gt;&lt;div&gt;&lt;br &#x2f;&gt;&lt;&#x2f;div&gt;&lt;&#x2f;div&gt;","id":"97709xxxxxxxxxxx","commenterId":"97709xxxxxxxxxxx","commenter":{"id":"97709xxxxxxxxxxx","name":"TIP Labops","email":"tip.labops@siemplify.co","photoURL":"https://desk.zoho.eu/api/v1/agents/97709xxxxxxxxxxx/photo?orgId=2008xxxxxx","type":"AGENT","firstName":"TIP","lastName":"Labops","roleName":"CEO"},"isPublic":false,"attachments":[]},{"content":"zsu[@user:115xxxxx]zsu Please fix this ASAP","commentedTime":"2022-07-01T11:18:44.000Z","modifiedTime":"2022-07-01T11:18:44.000Z","contentType":"plainText","impersonatedUser":null,"encodedContent":"zsu&#x5b;&#x40;user&#x3a;115xxxxx&#x5d;zsu Please fix this ASAP","id":"97709xxxxxxxxxxx","commenterId":"97709xxxxxxxxxxx","commenter":{"id":"97709xxxxxxxxxxx","name":"TIP Labops","email":"tip.labops@siemplify.co","photoURL":"https://desk.zoho.eu/api/v1/agents/97709xxxxxxxxxxx/photo?orgId=2008xxxxxxx","type":"AGENT","firstName":"TIP","lastName":"Labops","roleName":"CEO"},"isPublic":false,"attachments":[]}]}]
```



#### Mark Ticket As Spam
Mark ticket as spam in Zoho Desk.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify an id of the ticket that needs to be marked as spam.|True|String||
|Mark Contact|If enabled, the contact that created the ticket will be marked as spammer.|False|Boolean|true|



#### Update Ticket
Update a ticket in Zoho Desk.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify an id of the ticket that needs to be updated.|True|String||
|Title|Specify the title that should be set for the ticket.|False|String||
|Description|Specify the description for the ticket.|False|String||
|Department Name|Specify the name of the department that should be set for the ticket.|False|String||
|Contact|Specify the email of the contact for the ticket.|False|String||
|Assignee Type|Specify the type of the assignee. If “Agent” or “Team” is selected “Assignee Name” is required.|False|List||
|Assignee Name|Specify the name of the assignee for the ticket. For the agent type you can provide an email address or display name.|False|String||
|Resolution|Specify the resolution for the ticket.|False|String||
|Priority|Specify the priority for the ticket.|False|List||
|Status|Specify the status for the ticket.|False|List||
|Mark State|Specify the mark state for the ticket.|False|List||
|Classification|Specify the classification type for the ticket.|False|List||
|Channel|Specify the channel for the ticket.|False|List||
|Category|Specify the category for the ticket.|False|String||
|Sub Category|Specify the subcategory for the ticket.|False|String||
|Due Date|Specify the due date for the ticket. Format: ISO 8601. Example: 2022-07-06T07:05:43Z. Note: this parameter doesn’t have an impact, when status is “On Hold”.|False|String||
|Custom Fields|Specify a json object containing the custom fields that need to be added. Note: you need to provide the API names of the keys.|False|String||



##### JSON Results
```json
{  
    "modifiedTime": "2022-07-01T11:00:33.000Z",  
    "subCategory": null,  
    "statusType": "On Hold",  
    "subject": "Here's your first ticket.",  
    "dueDate": null,  
    "departmentId": "XXX0900000000XXXX",  
    "channel": "Chat",  
    "onholdTime": "2022-07-01T09:32:14.717Z",  
    "language": "English",  
    "source": {  
        "appName": null,  
        "extId": null,  
        "permalink": null,  
        "type": "SYSTEM",  
        "appPhotoURL": null  
    },  
    "resolution": "Koko",  
    "sharedDepartments": [],  
    "closedTime": null,  
    "approvalCount": "0",  
    "isOverDue": true,  
    "isTrashed": false,  
    "createdTime": "2022-06-27T17:02:17.000Z",  
    "id": "XXX0000000000XXXX",  
    "isResponseOverdue": false,  
    "customerResponseTime": "2022-06-27T17:02:17.000Z",  
    "productId": null,  
    "contactId": "XXX00000000000XXX",  
    "threadCount": "1",  
    "secondaryContacts": [],  
    "priority": null,  
    "classification": null,  
    "commentCount": "1",  
    "taskCount": "0",  
    "accountId": "XXX00000000000XXX",  
    "phone": "1 111 111 1111",  
    "webUrl": "https://desk.zoho.com/",  
    "isSpam": false,  
    "status": "On Hold",  
    "entitySkills": [],  
    "ticketNumber": "42",  
    "customFields": {},  
    "isArchived": false,  
    "description": "Hello<",  
    "timeEntryCount": "0",  
    "channelRelatedInfo": null,  
    "responseDueDate": null,  
    "isDeleted": false,  
    "modifiedBy": "XXX00000000000XXX",  
    "email": "support@zohosupport.com",  
    "layoutDetails": {  
        "id": "XXX00000000000XXX",  
        "layoutName": "Siemplify"  
    },  
    "channelCode": null,  
    "cf": {},  
    "slaId": null,  
    "layoutId": "XXX00000000000XXX",  
    "assigneeId": null,  
    "teamId": "XXX00000000000XXX",  
    "attachmentCount": "0",  
    "isEscalated": false,  
    "category": null  
}  

```



#### Create Ticket
Create a ticket in Zoho Desk.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Title|Specify the title for the ticket.|True|String||
|Description|Specify the description of the ticket.|True|String||
|Department Name|Specify the name of the department in which you want to create a ticket.|True|String||
|Contact|Specify the email of the contact for the ticket.|True|String||
|Assignee Type|Specify the type of the assignee. If "Agent" or "Team" is selected "Assignee Name" is required.|False|List|Select One|
|Assignee Name|Specify the name of the assignee for the ticket. For the agent type you can provide an email address or display name.|False|String||
|Priority|Specify the priority for the ticket.|False|List|No Priority|
|Classification|Specify the classification type for the ticket.|False|List|No Classification|
|Channel|Specify the channel for the ticket.|False|List|Email|
|Category|Specify the category for the ticket.|False|String||
|Sub Category|Specify the subcategory for the ticket.|False|String||
|Due Date|Specify the due date for the ticket. Format: ISO 8601. Example: 2022-07-06T07:05:43Z.|False|String||
|Custom Fields|Specify a json object containing the custom fields that need to be added. Note: you need to provide the API names of the keys.|False|String||



##### JSON Results
```json
{"modifiedTime":"2022-07-01T11:00:33.000Z","subCategory":null,"statusType":"On Hold","subject":"Here's your first ticket.","dueDate":null,"departmentId":"9770xxxxxxxxxxx","channel":"Chat","onholdTime":"2022-07-01T09:32:14.717Z","language":"English","source":{"appName":null,"extId":null,"permalink":null,"type":"SYSTEM","appPhotoURL":null},"resolution":"Koko","sharedDepartments":[],"closedTime":null,"approvalCount":"0","isOverDue":true,"isTrashed":false,"createdTime":"2022-06-27T17:02:17.000Z","id":"9770xxxxxxxxxxx","isResponseOverdue":false,"customerResponseTime":"2022-06-27T17:02:17.000Z","productId":null,"contactId":"9770xxxxxxxxxxx","threadCount":"1","secondaryContacts":[],"priority":null,"classification":null,"commentCount":"1","taskCount":"0","accountId":"9770xxxxxxxxxxx","phone":"1 888 xxx xxxx","webUrl":"https://desk.zoho.eu/support/siemplify/ShowHomePage.do#Cases/dv/9770xxxxxxxxxxx","isSpam":false,"status":"On Hold","entitySkills":[],"ticketNumber":"xxx","customFields":{},"isArchived":false,"description":"Hello<","timeEntryCount":"0","channelRelatedInfo":null,"responseDueDate":null,"isDeleted":false,"modifiedBy":"9770xxxxxxxxxxx","email":"support@zohosupport.com","layoutDetails":{"id":"9770xxxxxxxxxxx","layoutName":"Siemplify"},"channelCode":null,"cf":{},"slaId":null,"layoutId":"9770xxxxxxxxxxx","assigneeId":null,"teamId":"9770xxxxxxxxxxx","attachmentCount":"0","isEscalated":false,"category":null}
```



#### Add Comment To Ticket
Add a comment to a ticket in Zoho Desk. Note: Action is running as async if "Wait For Reply" is enabled, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ticket ID|Specify an id of the ticket to which you want to add a comment.|True|String||
|Visibility|Specify if the comment should be public or private.|False|List|Public|
|Type|Specify what should be the type of the comment.|False|List|Plain Text|
|Text|Specify the content of the comment.|True|String||
|Wait For Reply|If enabled, action will wait for reply.|False|Boolean|false|



##### JSON Results
```json
{"content":"zsu[@user:115xxxxx]zsu Please fix this ASAP","commentedTime":"2022-07-01T11:18:43.935Z","modifiedTime":"2022-07-01T11:18:43.935Z","contentType":"plainText","impersonatedUser":null,"encodedContent":"zsu&#x5b;&#x40;user&#x3a;115xxxxx&#x5d;zsu Please fix this ASAP","id":"9770xxxxxxxxxxxxx","commenterId":"9770xxxxxxxxxxxxx","commenter":{"id":"9770xxxxxxxxxxxxx","name":"TIP Labops","email":"tip.labops@siemplify.co","photoURL":"https://desk.zoho.eu/api/v1/agents/9770xxxxxxxxxxxxx/photo?orgId=2008xxxxxxxx","type":"AGENT","firstName":"TIP","lastName":"Labops","roleName":"CEO"},"attachments":[],"isPublic":false}
```









