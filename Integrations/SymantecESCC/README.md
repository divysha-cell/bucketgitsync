
# SymantecESCC

Symantec Endpoint Security Complete delivers the most comprehensive and integrated endpoint security platform on the planet. As an on premises, hybrid, or cloud-based solution, the single-agent Symantec platform protects all traditional and mobile endpoints, providing interlocking defenses at the device, application, and network level, and uses artificial intelligence (AI) to optimize security decisions. A unified cloud based management system simplifies protecting, detecting, and responding to all the advanced threats targeting your endpoints. This integration was designed for the cloud version of Symantec Endpoint Security Complete.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|URL|https://api.sep.securitycloud.symantec.com|
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|netaddr-1.3.0-py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|filelock-3.16.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich entities using information from Symantec Endpoint Security Complete. Supported entities: Hostname, Hash, URL and IP Address. Only SHA256 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Group|Specify the name of the device group that should be used to retrieve information about endpoints.|True|String|Default|
|Create Endpoint Insight|If enabled, action will create an insight containing information about the endpoints.|False|Boolean|true|
|Create IOC Insight|If enabled, action will create an insight containing information about enriched IOCs.|False|Boolean|true|



##### JSON Results
```json
[{"Entity":"DESKTOP-xxxxxx","EntityResult":{"id":"x10bQZJsRi6z87xxxxxx","os":{"ver":"10.0.18363","name":"Windows 10 Enterprise Edition","type":"WINDOWS_WORKSTATION","64_bit":true,"lang":"en","major_ver":10,"minor_ver":0,"sp":0,"tz_offset":-480,"user":"Admin","user_domain":"LocalComputer","vol_avail_mb":5443,"vol_cap_mb":30138},"name":"DESKTOP-xxxxxx","host":"DESKTOP-xxxxxx","domain":"WORKGROUP","created":"2020-11-19T12:24:23.422Z","modified":"2021-03-05T10:39:03.884Z","adapters":[{"addr":"00:50:56:xxxxxx","category":"Public","ipv4Address":"172.30.xxx.xxx","ipv4_gw":"172.30.xxx.xxx","ipv4_prefix":24,"ipv6Address":"fe80::9c8f:dc54:xxx:xxx","ipv6_gw":"172.30.xxx.xxx","ipv6_prefix":64,"mask":"255.255.255.0"}],"device_status":"SECURE","parent_device_group_id":"rujWDk9WTcKsnLxxxxxxx","products":[{"name":"Symantec Endpoint Protection","product_status":"SECURE","version":"14.3.3384.1000","agent_status":"ONLINE","last_connected_time":"2021-03-05T10:39:23.271Z","features":[{"name":"APP_ISOLATION","state":"ENABLED","feature_status":"SECURE","engine_version":"6.7.0.2033"},{"name":"FIREWALL","state":"ENABLED","feature_status":"SECURE"}]}]}},{"Entity":"67e5e54fadd769e106203edc4c08f15fd0a31b60ba6c8d9d383a9dfxxxxxxxx","EntityResult":{"reputation":"BAD","prevalence":"LessThanFifty","firstSeen":"2021-04-01","lastSeen":"2021-04-03","targetOrgs":{"topCountries":["us","cm","sg"],"topIndustries":["financial services"]},"state":"blocked","process_chain":[{"parent":{"parent":{"file":"6a671b92a69755de6fd063fcbe4ba926d83b49f78c42dbaeed8cdbxxxxxxxxxx","processName":"explorer.exe"},"file":"f686f2ff41923bb5c106c76d5f3df30146eb37683b81c4a57110dcxxxxxxxxxx","processName":"chrome.exe"}}]}}]
```



#### Ping
Test connectivity to the  Symantec Endpoint Security Complete with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Get Related IOCs
Get IOCs related to the entities from Symantec Endpoint Security Complete. Supported entities: Hash, URL and IP Address. Only SHA256 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source Filter|Specify the source filter. If nothing is provided, action will return related entities, based on all sources. Possible Values: byThreatActor, byProcessChain, bySignature, bySampleTraits, byNetworkingTrait, bySimilarIncidents.|False|String|byThreatActor,byProcessChain,bySignature,bySampleTraits,byNetworkingTrait,bySimilarIncidents|



##### JSON Results
```json
{"total_file_IOCs":["2b6dc1a826a4d5d5de5a30b458e6ed995a4cfb9cad8114dxxxxxxxxxxxxxxx","d431b8c8cd87d7bd7d3f88aaf2dacadc1d8553c29b1b970657xxxxxxxxxxxxx"],"total_domain_IOCs":["asdasd.com","testtest.net"],"total_IP_IOCs":["172.0.xxx.xxx","168.1.xxx.xxx"]}
```



#### List Device Groups
List available device groups in Symantec Endpoint Security Complete.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter.|False|String||
|Max Groups To Return|Specify how many groups to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"id":"rujWDk9WTcxxxxxxxxxxxx","name":"Default","created":"2020-11-19T02:17:15.236Z","modified":"2020-11-19T02:17:17.482Z","parent_id":""}]
```









