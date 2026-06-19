
# SymantecATP

Symantec Advanced Threat Protection (ATP) performs the critical security tasks that detect, protect, and respond to threats to your network.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|URL|https://x.x.x.x/|
|Client ID||True|Password|*****|
|Client Secret||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|tzdata-2026.2-py2.py3-none-any.whl|
|arrow-1.4.0-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Add Comment To Incident
Attach comment to incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident UUID|Specify the UUID of the incident.|True|String||
|Comment|Specify the comment that you want to add to the incident. Limit is 512 characters. This is Symantec ATP limitation.|True|String||



#### Add To Blacklist
Create a blacklist policy for an entity
Timeout - 600 Seconds



#### Get Events Free Query
Fetch events by free query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Free query text.|True|String|None|
|Limit|Limit of query results. Note: Limit is 5000 events. This is Symantec ATP limitation.|True|String|None|



#### Delete Blacklist Policy
Delete a blacklist policy for a Siemplify entity.
Timeout - 600 Seconds



#### Delete WhiteList Policy
Delete WhiteList policy for entity.
Timeout - 600 Seconds



#### Get Commands Status
Get status of a command
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Commands IDs|Command ID to fetch the status for.|True|String||



#### Enrich File Hash
Enrich SHA2 hash using Symantec ATP information.
Timeout - 600 Seconds



#### Get Incident Comments
Retrieve comments related to the incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident UUID|Specify the UUID of the incident.|True|String||
|Max Comments To Return|Specify how many comments to return. Maximum is 1000 comments. This is a Symantec ATP limitation. |False|String|20|



##### JSON Results
```json
{"comment": "awawdaq", "user_id": "100000", "incident_responder_name": "SEDR API", "time": "2020-05-18T08:17:18.895Z"}
```



#### Get Sandbox Commands Status
Get commands status by id.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Commands IDs|Sandbox Command ID to fetch the status for.|True|String||



#### Add To WhiteList
Create new whitelist policy. Note: MD5 hashes couldn’t be added to the whitelist, it's the Symantec ATP limitation.
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Isolate Endpoint
Isolate an endpoint on Symantec Endpoint Protection
Timeout - 600 Seconds



#### Rejoin Endpoint
Rejoin endpoint in Symantec Endpoint Protection
Timeout - 600 Seconds



#### Revoke From Blacklist
Delete blacklist policy for a given entity
Timeout - 600 Seconds



#### Submit Files To Sandbox
Submit file hashes to sandbox.
Timeout - 600 Seconds



#### Update Incident Resolution
Update resolution on the incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident UUID|Specify the UUID of the incident.|True|String||
|Resolution Status|Specify what resolution status to set on the incident.|True|List|INSUFFICIENT DATA|



#### Delete File
Delete file from an endpoint
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Hash|File hash to delete.|True|String||



#### Get Events  For Entity
Fetch all events for an entity since time
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Minutes Back To Fetch|Fetch the event x minutes back. Limit is 7 days, or 10080 minutes. This is Symantec ATP limitation.|True|String|None|



#### Close Incident
Change incident status to closed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident UUID|Specify the UUID of the incident|True|String||









## Connectors
#### Symantec ATP - Incidents Connector
Fetch incidents from Symantec ATP

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of Symantec ATP server.|True|String|https://x.x.x.x:port|
|Client ID|Symantec ATP Client ID|True|Password|*****|
|Client Secret|Symantec ATP Client Secret|True|Password|*****|
|Priority Filter|Priority filter for the incidents. If you want to ingest all of the incidents specify: Low, Medium, High.|True|String|Low, Medium, High|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Limit: 30 days. This is a Symantec ATP limitation.|False|Int|1|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Max: 1000.|False|Int|25|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Use SSL|Option to enable SSL/TLS connection|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use|False|String||
|Proxy Username|The proxy username to authenticate with|False|String||
|Proxy Password|The proxy password to authenticate with|False|Password|*****|




