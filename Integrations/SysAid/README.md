
# SysAid

SysAid is an IT service management solution that offers all the ITIL essentials. It's everything you need for easy and efficient ITSM in a single tool.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://{account}.sysaidit.com/api/v1|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.7.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Get Service Request
Get a service request.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Request ID|The ID of the service request to get info about.|True|String||



#### Update Service Request
Update a service request.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Request ID|The id of the service request to update.|True|String||
|Status|The new status of the request service.|False|String||
|Priority|The new priority of the request service.|False|String||
|Assignee|The new assignee of the request service.|False|String||
|Urgency|The new urgency of the request service.|False|String||
|Request User|The new request user of the request service.|False|String||
|Category|The new category of the request service.|False|String||
|Subcategory|The new subcategory of the request service.|False|String||
|Third Category|The new third category of the request service.|False|String||
|Assigned Group|The new assigned group of the request service.|False|String||



#### Delete Service Request
Delete a service request.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Request ID|The ID of the service request to delete.|True|String||



#### Close Service Request
Close a service request.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Request ID|The ID of the service request to delete.|True|String||
|Solution|The solution of the request service.|True|String||



#### Create Service Request
Create a service request.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Title|The title of the service request.|True|String||
|Description|The description of the service request.|True|String||
|Service Request Type|The type of the service request. Valid values: incident, request, problem, change, all.|False|String||
|Status|The status of the request service.|True|String||
|Priority|The priority of the request service.|True|String||
|Assignee|The assignee of the request service.|True|String||
|Urgency|The urgency of the request service.|True|String||
|Request User|The request user of the request service.|False|String||
|Category|The category of the request service.|False|String||
|Subcategory|The subcategory of the request service.|False|String||
|Third Category|The third category of the request service.|False|String||
|Assigned Group|The assigned group of the request service.|False|String||



#### List Service Requests
List service requests.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Request Type|The type of the service request to filter by. Valid values: incident, request, problem, change, all.|False|String||
|Status|The status of the request service to filter by.|False|String||
|Priority|The priority of the request service to filter by.|False|String||
|Assignee|The assignee of the request service to filter by.|False|String||
|Urgency|The urgency of the request service to filter by.|False|String||
|Request User|The request user of the request service to filter by.|False|String||
|Category|The category of the request service to filter by.|False|String||
|Subcategory|The subcategory of the request service to filter by.|False|String||
|Third Category|The third category of the request service to filter by.|False|String||
|Assigned Group|The assigned group of the request service to filter by.|False|String||
|Get Archived|Whether to get archived request services or not.|False|Boolean||



#### Ping
Test SysAid connectivity.
Timeout - 600 Seconds



#### List Users
List SysAid users.
Timeout - 600 Seconds









