
# StellarCyberStarlight

Stellar Cyber is the only open, automated detection and response platform that correlates detections from existing solutions as well as its own security applications to deliver comprehensive protection across the cybersecurity kill chain and present them through one intuitive dashboard. Customers can leverage 20 native applications and a growing list of open ecosystem partners to detect and respond automatically to attacks within seconds wherever they occur â€“ on servers, in the network, at endpoints, or in cloud-based applications. Stellar Cyber deploys easily on premises, in public clouds or with service providers.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://{ip address}/connect/api/|
|Username||True|String||
|API Key|API Key of the Stellar Cyber Starlight account. This parameter was used for Basic Authentication. If both “API Key” and “API Token” is provided, “API Token” will have priority.|False|Password|*****|
|API Token|API Token of the Stellar Cyber Starlight account. This parameter was used for JWT Authentication. If both “API Key” and “API Token” is provided, “API Token” will have priority.|False|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|certifi-2026.5.20-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.16-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|


## Actions
#### Simple Search
Perform simple search in Stellar Cyber Starlight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Specify in which index do you want to search. You can find a list of known indexes in the documentation.|True|String||
|Query|Specify query filter for the search.|True|String||
|Max Results To Return|Specify how many results to return in response.|False|String|50|
|Sort Field|Specify the field, which should be used for sorting.|False|String||
|Sort Order|Specify the sort order for the result.|False|List|Descending|



##### JSON Results
```json
[{"_index": "aella-assets-2020.07.10", "_type": "amsg", "_id": "6ada4b1e-c21b-11ea-ba27-c2317d2axxxx", "_score": null, "_source": {"ip": "172.30.203.xxx", "locid": "unassigned location", "tenantid": "", "tag": "", "start_time_date": "2020-07-09 19:34:18", "device_class": "", "id": "6ada4b1e-c21b-11ea-ba27-c2317d2axxxx", "service": [], "engid": "ad42005056a2xxxx", "state": "new", "device_desc": "", "applist": [], "iplist": ["172.30.203.xxx"], "desc": "", "apphistory": [], "location": "Tel Aviv,Israel", "vendor": "Fortinet, Inc.\r", "user_sid": "", "timestamp": 1594323438160, "start_time": 1594323258153, "vlan": 0, "mac": "e8:1c:ba:4c:37:xx", "d": {"appid_id": "", "type": "host"}, "name": "172.30.203.xxx", "iphistory": [{"ip": "172.30.203.xxx", "time": 1594323258153}], "geoip": "185.180.102.xxx", "subtype": "client", "last_seen_date": "2020-07-09 19:37:18", "reputation": "Good", "t": "172.30.203.xxx", "last_seen": 1594323438160}, "sort": [1594323438160]}, {"_index": "aella-assets-2020.07.10", "_type": "amsg", "_id": "8569172c-c210-11ea-ada3-c2317d2axxxx", "_score": null, "_source": {"ip": "172.30.202.xxx", "locid": "unassigned location", "tenantid": "", "tag": "", "start_time_date": "2020-07-09 18:16:17", "device_class": "", "id": "8569172c-c210-11ea-ada3-c2317d2axxxx", "service": [], "engid": "ad42005056a2xxxx", "state": "new", "device_desc": "", "applist": [], "iplist": ["172.30.202.xxx"], "desc": "", "apphistory": [], "location": "Tel Aviv,Israel", "vendor": "VMware, Inc.\r", "user_sid": "", "timestamp": 1594339278823, "start_time": 1594318577932, "vlan": 0, "mac": "00:50:56:a2:04:xx", "d": {"appid_id": "", "type": "host"}, "name": "172.30.202.xxx", "iphistory": [{"ip": "172.30.202.xxx", "time": 1594318577932}], "geoip": "185.180.102.xxx", "subtype": "client", "last_seen_date": "2020-07-10 00:01:18", "reputation": "Good", "t": "172.30.202.xxx", "last_seen": 1594339278823}, "sort": [1594339278823]}]
```



#### Update Security Event
Update security event in Stellar Cyber Starlight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Specify the index of the security event.|True|String||
|ID|Specify the ID of the security event.|True|String||
|Comment|Specify a comment for the security event.|False|String||
|Status|Specify the new status for the security event.|True|List|Select One|



#### Advanced Search
Perform advanced search in Stellar Cyber Starlight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Specify in which index do you want to search. You can find a list of known indexes in the documentation.|True|String||
|DSL Query|Specify the json object of the DSL query that you want to execute.|True|String|{
    "size": 1,
    "from": 0,
    "query": {
        "match_all": {}
    },
    "sort": [
        {
            "timestamp": {
                "order": "asc"
            }
        }
    ]
}
|



##### JSON Results
```json
[{"_index": "aella-assets-2020.07.10", "_type": "amsg", "_id": "6ada4b1e-c21b-11ea-ba27-c2317d2axxxx", "_score": null, "_source": {"ip": "172.30.203.xxx", "locid": "unassigned location", "tenantid": "", "tag": "", "start_time_date": "2020-07-09 19:34:18", "device_class": "", "id": "6ada4b1e-c21b-11ea-ba27-c2317d2axxxx", "service": [], "engid": "ad42005056a2xxxx", "state": "new", "device_desc": "", "applist": [], "iplist": ["172.30.203.xxx"], "desc": "", "apphistory": [], "location": "Tel Aviv,Israel", "vendor": "Fortinet, Inc.\r", "user_sid": "", "timestamp": 1594323438160, "start_time": 1594323258153, "vlan": 0, "mac": "e8:1c:ba:4c:37:xx", "d": {"appid_id": "", "type": "host"}, "name": "172.30.203.xxx", "iphistory": [{"ip": "172.30.203.xxx", "time": 1594323258153}], "geoip": "185.180.102.xxx", "subtype": "client", "last_seen_date": "2020-07-09 19:37:18", "reputation": "Good", "t": "172.30.203.xxx", "last_seen": 1594323438160}, "sort": [1594323438160]}, {"_index": "aella-assets-2020.07.10", "_type": "amsg", "_id": "8569172c-c210-11ea-ada3-c2317d2axxxx", "_score": null, "_source": {"ip": "172.30.202.xxx", "locid": "unassigned location", "tenantid": "", "tag": "", "start_time_date": "2020-07-09 18:16:17", "device_class": "", "id": "8569172c-c210-11ea-ada3-c2317d2axxxx", "service": [], "engid": "ad42005056a2xxxx", "state": "new", "device_desc": "", "applist": [], "iplist": ["172.30.202.xxx"], "desc": "", "apphistory": [], "location": "Tel Aviv,Israel", "vendor": "VMware, Inc.\r", "user_sid": "", "timestamp": 1594339278823, "start_time": 1594318577932, "vlan": 0, "mac": "00:50:56:a2:04:xx", "d": {"appid_id": "", "type": "host"}, "name": "172.30.202.xxx", "iphistory": [{"ip": "172.30.202.xxx", "time": 1594318577932}], "geoip": "185.180.102.xxx", "subtype": "client", "last_seen_date": "2020-07-10 00:01:18", "reputation": "Good", "t": "172.30.202.xxx", "last_seen": 1594339278823}, "sort": [1594339278823]}]
```



#### Ping
Test connectivity to Stellar Cyber Starlight with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Stellar Cyber Starlight - Security Events Connector
Pull security events from Stellar Cyber Starlight.  Note: dynamic list works with the Chronicle SOAR alert name, which can be either “event_category: event_name” or “_source_xdr_event_xdr_killchain_stage:_source_xdr_event_name”

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|_source_event_name|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API Root of the Stellar Cyber Starlight instance.|True|String|https://{ip}/connect/api/|
|Username|Username of the Stellar Cyber Starlight account.|True|String||
|API Key|API Key of the Stellar Cyber Starlight account. This parameter was used for Basic Authentication. If both “API Key” and “API Token” is provided, “API Token” will have priority.|False|Password|*****|
|API Token|API Token of the Stellar Cyber Starlight account. This parameter was used for JWT Authentication. If both “API Key” and “API Token” is provided, “API Token” will have priority.|False|Password|*****|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch events.|True|Integer|50|
|Padding Period|Padding period (hours) for the connector execution.|False|Integer|0|
|Max Events To Fetch|How many events to process per one connector iteration.|False|Integer|50|
|Timestamp Field|Field that will be used for managing time in the connector. Supported values: timestamp, write_time|True|String|timestamp|
|Product Field Fallback|Specify a comma separated list of incident or alert attributes that should be used as a fallback for the "Product Field Name" parameter and "DeviceProduct" field in descending order. First attribute will have the highest priority, next if its not present or empty in the event - fallback to the next value from the list and so on.|False|String||
|Event Field Fallback|Specify a comma separated list of alert attributes that should be used as a fallback for the "Event Field Name" parameter in descending order. First attribute will have the highest priority, next if it's not present or empty in the event - fallback to the next value from the list and so on. Note: this parameter will introduce a new key in the event data called "chronicle_event_type". Use this key in the "Event Field Name" parameter to be able to utilize the fallback logic.|False|String||
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Stellar Cyber Starlight server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




