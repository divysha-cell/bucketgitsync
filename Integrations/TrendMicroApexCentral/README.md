
# TrendMicroApexCentral

Trend Micro Apex Central™ is a web-based console that provides centralized management for Trend Micro products and services at the gateway, mail server, file server, and corporate desktop levels. Administrators can use the policy management feature to configure and deploy product settings to managed products and endpoints. The Apex Central web-based management console provides a single monitoring point for antivirus and content security products and services throughout the network.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://pbxpp4.manage.trendmicro.com/|
|Application ID||True|String||
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|validators-0.33.0-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|PyJWT-2.9.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Create Entity UDSO
Create a User-defined suspicious object based on the entities in Trend Micro Apex Central. Supported entities: IP, URL, Hash. Note: only SHA-1 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Action|Specify what action should be applied to the UDSO.|True|List|Block|
|Note|Specify an additional note for the provided UDSO. Warning: this note can't contain more than 256 characters.|False|String||
|Expire In (Days)|Specify in how many days the UDSO should expire. If nothing is provided, UDSO will never expire.|False|String||



##### JSON Results
```json
[{"Entity": "X.X.X.X.X", "EntityResult": {"type": "ip", "content": "X.X.X.X.X", "notes": "my note", "scan_action": "log", "expiration_utc_date": "2021-03-26T12:26:49.753"}}]
```



#### Enrich Entities
Enrich entities with information from Trend Micro Apex Central. Supported entities: IP Address, MAC Address, Hostname, URL, Hash. Note: only SHA-1 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Endpoint Insight|If enabled, action will create an insight consisting of the information regarding the endpoints that were enriched.|False|Boolean|True|
|Create UDSO Insight|If enabled, action will create an insight consising of the information regarding the entities that matched UDSO.|False|Boolean|True|
|Mark UDSO Entities|If enabled, action will mark all of the entities that were seen in the User-Defined Suspicious Objects list as suspicious.|False|Boolean|True|
|Extract Domain|If enabled, action will extract domain part of the URL entity and use it for enrichment.|False|Boolean|False|



##### JSON Results
```json
[{"Entity": "XXX.XX.XXX.XXX", "EntityResult": {"type": "ip", "content": "XXX.XX.XXX.XXX", "notes": "mynote", "scan_action": "log", "expiration_utc_date": "None", "entity_id": "XXX.XX.XXX.XXX", "product": "XXXX_XXX_XXX", "managing_server_id": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXX", "ad_domain": "", "folder_path": "Workgroup", "ip_address_list": "XXX.XX.XXX.XXX", "mac_address_list": "XX-XX-XX-XX-XX-XX", "host_name": "DESKTOP-XXXXXX", "isolation_status": "endpoint_isolation_pending", "capabilities": ["cmd_restore_isolated_agent", "cmd_isolate_agent", "cmd_relocate_agent", "cmd_uninstall_agent"]}}, {"Entity": "XXX.XX.XXX.XXX", "EntityResult": {"entity_id": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXX", "product": "XXX_XXXX_XXX", "managing_server_id": "XXXXXXX-XXXX-XXXX-XXXX-XXXXXXX", "ad_domain": "", "folder_path": "Siemplifylab", "ip_address_list": "XXX.XX.XXX.XXX", "mac_address_list": "XX-XX-XX-XX-XX-XX", "host_name": "XXXXXX", "isolation_status": "normal", "capabilities": ["cmd_restore_isolated_agent", "cmd_isolate_agent", "cmd_relocate_agent", "cmd_uninstall_agent"]}}]
```



#### Isolate Endpoints
Isolate endpoints in Trend Micro Apex Central. Supported entities: IP Address, Hostname, MAC Address. Note: this action can take several minutes to finish, so consider increasing the timeout in the IDE.
Timeout - 600 Seconds



#### Create File UDSO
Create a User-defined suspicious object based on a file in Trend Micro Apex Central.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|Specify a comma-separated list of file paths that needs to be used to create a UDSO.|True|String||
|Action|Specify what action should be applied to the UDSO.|True|List|Block|
|Note|Specify an additional note for the provided UDSO.|False|String||



##### JSON Results
```json
[{"Entity": "XXXXXXXXXXXXXXXXXXXXXXX", "EntityResult": {"type": "file", "content": "XXXXXXXXXXXXXXXXXXXXXXX", "notes": "", "scan_action": "log", "expiration_utc_date": "2021-03-26T12:26:49.753"}}]
```



#### Ping
Test connectivity to the Trend Micro Apex Central with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Unisolate Endpoints
Unisolate endpoints in Trend Micro Apex Central. Supported entities: IP Address, Hostname, MAC Address. Note: this action can take several minutes to finish, so consider increasing the timeout in the IDE.
Timeout - 600 Seconds









