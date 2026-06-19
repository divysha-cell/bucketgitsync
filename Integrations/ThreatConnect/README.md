
# ThreatConnect

Identify Manage and Block Threats Faster with Intelligence. Make informed decisions with ThreatConnect's in-platform analytics and automation.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ApiAccessId|None|True|Password|*****|
|ApiSecretKey|None|True|Password|*****|
|ApiDefaultOrg|None|True|String||
|ApiBaseUrl|None|True|String|https://sandbox.threatconnect.com/api|


#### Dependencies
| |
|-|
|setuptools-80.9.0-py3-none-any.whl|
|TIPCommon-1.0.16-py2.py3-none-any.whl|
|pytz-2024.1-py2.py3-none-any.whl|
|urllib3-2.0.7-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|threatconnect-2.4.21.tar.gz|
|python_dateutil-2.9.0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich IP addresses, hosts, URLs and hashes with information from ThreatConnect
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Owner Name|Owner name to fetch the data from. Parameter also accepts comma separated list of owner names.|False|String||



##### JSON Results
```json
[{"EntityResult": {"securityLabels": {"securityLabel": [], "resultCount": 0}, "owners": {"owner": [{"type": "Organization", "id": 440, "name": "S"}]}, "victims": {"resultCount": 0, "victim": []}, "tags": ["C2", "Malware"], "general": {"url": {"rating": 5.0, "confidence": 100, "dateAdded": "2018-01-09T20: 12: 11Z", "description": "URLAssociatedwithCryptoLockerC2Servers", "threatAssessConfidence": 93.33, "lastModified": "2018-01-09T20: 13: 24Z", "threatAssessRating": 4.33, "webLink": "https: //sandbox.threatconnect.com/auth/indicators/details/url.xhtml?orgid=43743075&owner=S", "text": "http: //markossolomon.com/f1q7qx.php", "owner": {"type": "Organization", "id": 440, "name": "S"}, "id": 43743075}}, "observations": {"resultCount": 0, "observation": []}, "groups": null, "indicators": {"indicator": [], "resultCount": 0}, "attributes": {"Description": ["URLAssociatedwithCryptoLockerC2Servers"]}, "observationCount": {"observationCount": {"count": 0}}, "victimAssets": {"victimAsset": [], "resultCount": 0}}, "Entity": "HTTP: //MARKOSSOLOMON.COM/F1Q7QX.PHP"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









