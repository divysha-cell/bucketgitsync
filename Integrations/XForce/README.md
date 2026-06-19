
# XForce

X-Force - Deep security research expertise and global threat intelligence for enhanced security solutions

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address||True|String||
|Api Key||True|String||
|Api Password||True|Password|*****|
|Verify SSL||False|Boolean||


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
#### Get Url Info
Query XForce for URL information
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Threshold must be an integer(e.g: 3).|False|String|1|



##### JSON Results
```json
[{"EntityResult": {"associated": [{"url": "domain-example.com", "cats": {}, "score": null, "categoryDescriptions": {}}], "result": {"url": "domain-example.com/f1q7qx.php", "cats": {"Botnet Command and Control Server": true}, "score": 10, "categoryDescriptions": {"Botnet Command and Control Server": "This category contains Web sites or domains that host a botnet command and control server."}}, "tags": []}, "Entity": "HTTP://DOMAIN_EXAMPLE.COM/F1Q7QX.PHP"}]
```



#### Ping
Test Connectivity to XForce
Timeout - 600 Seconds



#### Get IP Info
Query XForce for IP information
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Threshold must be an integer(e.g: 3).|False|String||



##### JSON Results
```json
[{"EntityResult": {"subnets": [{"subnet": "1.1.1.1/14", "reasonDescription": "One of the five RIRs announced a (new) location mapping of the IP.", "created": "2017-10-18T06:23:00.000Z", "ip": "1.1.1.1", "asns": {"8359": {"Company": "MTS, RU", "cidr": 14}}, "reason": "Regional Internet Registry", "score": 1, "categoryDescriptions": {}, "cats": {}, "geo": {"country": "Russia", "countrycode": "RU"}}, {"subnet": "1.1.1.1/20", "reasonDescription": "Based on statistical DNS analysis.", "created": "2014-01-22T19:56:00.000Z", "ip": "1.1.1.1", "reason": "DNS heuristics", "score": 1, "categoryDescriptions": {"Dynamic IPs": "This category contains IP addresses of dialup hosts and DSL lines."}, "cats": {"Dynamic IPs": 71}}], "reasonDescription": "One of the five RIRs announced a (new) location mapping of the IP.", "tags": [], "ip": "1.1.1.1", "reason": "Regional Internet Registry", "score": 1, "categoryDescriptions": {"Dynamic IPs": "This category contains IP addresses of dialup hosts and DSL lines."}, "cats": {"Dynamic IPs": 71}, "geo": {"country": "Russia", "countrycode": "RU"}, "history": [{"reasonDescription": "One of the five RIRs announced a (new) location mapping of the IP.", "created": "2012-03-22T07:26:00.000Z", "ip": "1.1.1.1/14", "reason": "Regional Internet Registry", "score": 1, "categoryDescriptions": {}, "cats": {}, "geo": {"country": "Russia", "countrycode": "RU"}}, {"reasonDescription": "Based on statistical DNS analysis.", "created": "2012-04-13T13:34:00.000Z", "ip": "1.1.1.1/14", "reason": "DNS heuristics", "score": 1, "categoryDescriptions": {"Dynamic IPs": "This category contains IP addresses of dialup hosts and DSL lines."}, "cats": {"Dynamic IPs": 100}, "geo": {"country": "Russia", "countrycode": "RU"}}, {"reasonDescription": "Based on statistical DNS analysis.", "created": "2014-01-22T19:56:00.000Z", "ip": "1.1.1.1/20", "reason": "DNS heuristics", "score": 1, "categoryDescriptions": {"Dynamic IPs": "This category contains IP addresses of dialup hosts and DSL lines."}, "cats": {"Dynamic IPs": 71}, "geo": {"country": "Russia", "countrycode": "RU"}}]}, "Entity": "1.1.1.1"}]
```



#### Get IP By Category

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category|Category for IP.|True|String|None|



##### JSON Results
```json
[{"ip": "string", "score": "integer", "created": "string"}]
```



#### Get IP Malware
Query XForce for the malware associated with an IP address
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"malware": [{"count": 13, "origin": "CnC", "domain": "domain-example.info", "last": "2016-10-29T06:31:00Z", "family": ["kasidet"], "filepath": "dom/tasks.php", "ip": "0x00000000000000000000ffff08080808", "uri": "http://domain-example.info/dom/tasks.php", "first": "2016-10-29T06:31:00Z", "host": "dom", "lastseen": "2016-10-29T06:31:00Z", "md5": "4C10F74CE20328B7CC4207245BC9D000", "type": "CnC", "firstseen": "2016-10-29T06:31:00Z", "schema": "http"}]}, "Entity": "1.1.1.1"}]
```



#### Get Hash Info
Query XForce for hash information
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|The value of the threshold can be: low, medium or high.|False|String||



##### JSON Results
```json
[{"EntityResult": {"malware": {"hash": "0x474B9CCF5AB9D72CA8A333889BBB3000", "family": ["tsunami"], "origins": {"downloadServers": {}, "subjects": {}, "CnCServers": {"count": 1, "rows": [{"count": 483, "origin": "CnC", "domain": "domain.net", "filepath": "v.html", "ip": "1.1.1.1", "uri": "http://domain.net/v.html", "lastseen": "2014-10-20T23:19:00Z", "md5": "474B9CCF5AB9D72CA8A333889BBB3000", "type": "CnC", "firstseen": "2014-10-20T23:19:00Z", "schema": "http"}]}, "emails": {}, "external": {"detectionCoverage": 46, "family": ["heuristic", "trojan"]}}, "created": "2014-10-20T23:19:00Z", "familyMembers": {"tsunami": {"count": 61}}, "md5": "0x474B9CCF5AB9D72CA8A333889BBB3000", "type": "md5", "risk": "high"}, "tags": []}, "Entity": "474B9CCF5AB9D72CA8A333889BBB3000"}]
```









