
# AlgoSec

Manage your network security effectively, swiftly, and confidently. No matter where your network lives. Gain complete visibility, automate changes, and always be compliant.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https:/{{ip address}}|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|TIPCommon-1.0.10-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|


## Actions
#### Allow IP
Allow IPs in AlgoSec. Supported entities: IP address. Note: IP address entities are treated as destinations in the change request. This action creates a traffic change request to allow traffic to IP entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Template|Specify the template for the change request.|True|String|Standard|
|Source|Specify a comma-separated list of sources for the allow rule. It can be an IP address, IP Set or special keyword like (all).|True|String|all|
|Service|Specify a comma-separated list of services that needs to be allowed. Values can have a look of {TCP/UDP}/{port} (tcp/80) or special reserved keyword (all).|True|String|ALL|
|Subject|Specify the subject for the change request. If nothing is provided action will put "Siemplify Allow IP request" in the subject.|False|String||
|Owner|Specify who should be the owner of the change request. If nothing is provided, the user that created the ticket will be the owner.|False|String||
|Due Date|Specify the due date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Expiration Date|Specify the expiration date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Custom Fields|Specify a JSON object containing information about all of the fields that need to be added to the change request. Note: this parameter has a priority over other fields|False|String||



##### JSON Results
```json
{"status": "Success", "messages": [], "data": {"id": 10, "fields": [{"name": "Owner", "values": ["admin<xxxxxxxx@siemplify.co>"]}, {"name": "Creator", "values": ["admin<xxxxxxxx@siemplify.co>"]}, {"name": "Due", "values": ["2021-08-31 00:00:00"]}, {"name": "LastUpdated", "values": ["2021-08-13 12:31:23"]}, {"name": "Requestor", "values": ["admin<xxxxxxxxxx@siemplify.co>"]}], "originalTraffic": [{"source": {"items": [{"value": "all"}]}, "destination": {"items": [{"value": "10.0.0.3"}]}, "service": {"items": [{"value": "ALL"}]}, "application": {"items": [{"value": "any"}]}, "user": {"items": [{"value": "any"}]}, "action": "Allow"}], "plannedTraffic": [{"source": {"items": [{"value": "0.0.0.0-255.255.255.255"}]}, "destination": {"items": [{"value": "10.0.0.3"}]}, "service": {"items": [{"value": "tcp/*"}, {"value": "udp/*"}, {"value": "ospf"}, {"value": "icmp/*"}, {"value": "gre"}, {"value": "ipsec_50"}, {"value": "ipsec_51"}]}, "application": {"items": [{"value": "any"}]}, "user": {"items": [{"value": "any"}]}, "action": "Allow"}]}}
```



#### Block IP
Block IPs in AlgoSec. Supported entities: IP address. Note: IP address entities are treated as destinations in the change request. This action creates a traffic change request to block traffic to IP entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Template|Specify the template for the change request.|True|String|Standard|
|Source|Specify a comma-separated list of sources for the block rule. It can be an IP address, IP Set or special keyword like (all).|True|String|all|
|Service|Specify a comma-separated list of services that needs to be blocked. Values can have a look of {TCP/UDP}/{port} (tcp/80) or special reserved keyword (all).|True|String|ALL|
|Subject|Specify the subject for the change request. If nothing is provided action will put “Siemplify Block IP request” in the subject.|False|String||
|Owner|Specify who should be the owner of the change request. If nothing is provided, the user that created the ticket will be the owner.|False|String||
|Due Date|Specify the due date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Expiration Date|Specify the expiration date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Custom Fields|Specify a JSON object containing information about all of the fields that need to be added to the change request. Note: this parameter has a priority over other fields|False|String||



##### JSON Results
```json
{"status": "Success", "messages": [], "data": {"id": 10, "fields": [{"name": "Owner", "values": ["admin<xxxxxxxx@siemplify.co>"]}, {"name": "Creator", "values": ["admin<xxxxxxxx@siemplify.co>"]}, {"name": "Due", "values": ["2021-08-31 00:00:00"]}, {"name": "LastUpdated", "values": ["2021-08-13 12:31:23"]}, {"name": "Requestor", "values": ["admin<xxxxxxxxxx@siemplify.co>"]}], "originalTraffic": [{"source": {"items": [{"value": "all"}]}, "destination": {"items": [{"value": "10.0.0.3"}]}, "service": {"items": [{"value": "ALL"}]}, "application": {"items": [{"value": "any"}]}, "user": {"items": [{"value": "any"}]}, "action": "Allow"}], "plannedTraffic": [{"source": {"items": [{"value": "0.0.0.0-255.255.255.255"}]}, "destination": {"items": [{"value": "10.0.0.3"}]}, "service": {"items": [{"value": "tcp/*"}, {"value": "udp/*"}, {"value": "ospf"}, {"value": "icmp/*"}, {"value": "gre"}, {"value": "ipsec_50"}, {"value": "ipsec_51"}]}, "application": {"items": [{"value": "any"}]}, "user": {"items": [{"value": "any"}]}, "action": "Allow"}]}}
```



#### Wait for Change Request Status Update
Wait for change request status update in AlgoSec. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed. Only traffic change requests are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|Specify the id of the request for which action needs to check the status.|True|String||
|Status|Specify a comma-separated list of change request statuses for which action should wait. Possible values: resolved, reconcile, open, check, implementation plan, implement, validate.|True|String|resolved|



##### JSON Results
```json
{"status": "Success", "messages": [], "data": {"id": 10, "fields": [{"name": "Owner", "values": ["admin<xxxxxxxx@siemplify.co>"]}, {"name": "Creator", "values": ["admin<xxxxxxxx@siemplify.co>"]}, {"name": "Due", "values": ["2021-08-31 00:00:00"]}, {"name": "LastUpdated", "values": ["2021-08-13 12:31:23"]}, {"name": "Requestor", "values": ["admin<xxxxxxxxx@siemplify.co>"]}], "originalTraffic": [{"source": {"items": [{"value": "all"}]}, "destination": {"items": [{"value": "10.0.0.3"}]}, "service": {"items": [{"value": "ALL"}]}, "application": {"items": [{"value": "any"}]}, "user": {"items": [{"value": "any"}]}, "action": "Allow"}], "plannedTraffic": [{"source": {"items": [{"value": "0.0.0.0-255.255.255.255"}]}, "destination": {"items": [{"value": "10.0.0.3"}]}, "service": {"items": [{"value": "tcp/*"}, {"value": "udp/*"}, {"value": "ospf"}, {"value": "icmp/*"}, {"value": "gre"}, {"value": "ipsec_50"}, {"value": "ipsec_51"}]}, "application": {"items": [{"value": "any"}]}, "user": {"items": [{"value": "any"}]}, "action": "Allow"}]}}
```



#### Ping
Test connectivity to the AlgoSec with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### List Templates
List available templates in AlgoSec.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Templates To Return|Specify how many templates to return. Default: 50.|False|String|50|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||



##### JSON Results
```json
[{"id": 142, "name": "110: Multi-Approval Request", "description": "Create a traffic change request which requires multiple approvals", "type": "Traffic Change", "enabled": true}, {"id": 597, "name": "190: Verbatim Rule Addition", "description": "Create a traffic change request for bulk rules addition exactly as specified", "type": "Traffic Change", "enabled": true}, {"id": 550, "name": "Basic Change Traffic Request", "description": "Create a basic change traffic request", "type": "Traffic Change", "enabled": true}]
```









