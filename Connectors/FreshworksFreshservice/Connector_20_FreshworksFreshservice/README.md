# Connector_20_FreshworksFreshservice
Connector can be used to fetch Freshservice tickets to create Siemplify alerts from. Connector whitelist can be used to ingest only specific types of tickets - Incident or Service Request


Integration: FreshworksFreshservice

Integration Version: 19

Device Product Field: Product Name

Event Name Field: type
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|API Root|Freshservice instance API Root.|True|https://yourdomain.freshservice.com|
|API Key|Freshservice API Key to use in integration.|True|*****|
|Verify SSL|If enabled, integration will try to verify that API Root is configured with a valid certificate.|False|true|
|Offset time in hours|Number of hours before the first connector iteration to retrieve tickets from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|24|
|Max Tickets Per Cycle|How many tickets should be processed during one connector run.|True|30|
|Minimum Priority to Fetch|Minimum priority of the ticket to be ingested to Siemplify, for example, Low or Medium. Possible values: Low, Medium, High, Urgent|False|5|
|Tickets Status to Fetch|Ticket statuses to be ingested to Siemplify. Parameter accepts multiple values as a comma separated string. Possible values: Open, Pending, Resolved, Closed|False|Open, Closed|
|Use dynamic list as a blocklist|If enabled, dynamic list will be used as a blocklist.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|Workspace ID|ID of the workspace that should be used to fetch tickets. If nothing is provided, the action will fetch tickets only from the primary workspace. To fetch tickets from all workspaces provide “0” in the parameter.|False|dummy_valid_string|

