
# URLVoid

URLVoid is a service that analyzes a website through multiple blacklist engines and online reputation tools to facilitate the detection of fraudulent and malicious websites.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ApiUrl||True|String|https://endpoint.apivoid.com|
|ApiKey||True|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.7.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Get domain reputation
Check if a domain is blacklisted by popular and trusted domain blacklist services.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Domain risk threshold.|True|String|0|



##### JSON Results
```json
[{"EntityResult": {"alexa_top_100k": false, "domain_length": 17, "alexa_top_10k": false, "blacklists": {"scantime": "0.07", "detection_rate": "0%", "detections": 0, "engines_count": 29, "engines": [{"engine": "ThreatLog", "detected": false, "confidence": "high", "reference": "http://www.threatlog.com/"}, {"engine": "Threat Sourcing", "detected": false, "confidence": "high", "reference": "https://www.threatsourcing.com/"}, {"engine": "URLVir", "detected": false, "confidence": "high", "reference": "http://www.urlvir.com/"}]}, "server": {"region_name": null, "reverse_dns": "", "ip": "", "isp": null, "continent_code": null, "latitude": null, "city_name": null, "longitude": null, "country_code": null, "country_name": null, "continent_name": null}, "host": "qotaerltozres.com", "most_abused_tld": false, "alexa_top_250k": false}, "Entity": "qotaerltozres.com"}, {"EntityResult": {"alexa_top_100k": false, "domain_length": 9, "alexa_top_10k": false, "blacklists": {"scantime": "0.03", "detection_rate": "0%", "detections": 0, "engines_count": 29, "engines": [{"engine": "ThreatLog", "detected": false, "confidence": "high", "reference": "http://www.threatlog.com/"}, {"engine": "Threat Sourcing", "detected": false, "confidence": "high", "reference": "https://www.threatsourcing.com/"}, {"engine": "URLVir", "detected": false, "confidence": "high", "reference": "http://www.urlvir.com/"}]}, "server": {"region_name": null, "reverse_dns": "", "ip": "", "isp": null, "continent_code": null, "latitude": null, "city_name": null, "longitude": null, "country_code": null, "country_name": null, "continent_name": null}, "host": "1.1.1.1", "most_abused_tld": false, "alexa_top_250k": false}, "Entity": "1.1.1.1"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









