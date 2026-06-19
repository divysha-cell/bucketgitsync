
# SymantecICDX

Symantec Integrated Cyber Defense Exchange (ICDx) is an open platform that gives you control over your enterprise security data: how much you collect, how long you retain it, and where it resides. It also provides a standard, cross-product schema for analytics, reports, and dashboards.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://{IP}:{PORT}|
|Api Token||True|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|arrow-1.4.0-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|charset_normalizer-3.4.6-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|tzdata-2025.3-py2.py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|


## Actions
#### Ping
Test SymantecICDX connectivity.
Timeout - 600 Seconds



#### Get Events Minutes Back
Get events for query, minutes back.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Request query.|True|String|None|
|Limit|Received events amount limit.|False|String|None|
|Minutes Back|Fetch events minutes back parameter.|False|String|None|
|Fields|Specific event fields to bring(Comma separated.)|False|String|None|



#### Get Event
Get event data by it's ID. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event UUID|Event UUID|True|String|None|









## Connectors
#### SymantecICDX query Connector
Fetching events from SymantecICDX server using a query

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|Api Root|True|String||
|Api Token|Api Token|True|Password|*****|
|Verify SSL|Whether to use ssl on connection or not|False|Boolean|FALSE|
|Search Query|Search Query|True|String||
|Events Limit|Max count of events to pull in one cycle. e.g. 20|True|Int|10|
|Max Days Backwards|Max number of days to fetch events since. e.g. 3|True|Int|1|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




