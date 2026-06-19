
# SymantecEmailSecurityCloud

Symantec™ Email Security.cloud is a complete email security solution that safeguards cloud email such as Office 365 and G Suite and on-premises email such as Microsoft Exchange. It blocks new and sophisticated email threats such as ransomware, spear phishing, and BEC with a multilayered defense and insights from the world’s largest civilian global intelligence network.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOC API Root|IOC API root of the Symantec Email Security.Cloud instance.|True|String|https://iocapi.emailsecurity.symantec.com|
|Username|Username of the Symantec Email Security.Cloud instance.|True|String||
|Password|Password of the Symantec Email Security.Cloud instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Symantec Email Security.Cloud server is valid.|False|Boolean|true|


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
#### Block Entities
Block entities in Symantec Email Security.Cloud. Supported entities: Hostname, IP address, URL, Filehash, Email Subject, Email Address (user entity that matches email regex). Note: only MD5 and SHA256 hashes are supported. All of the entities are treated as "sender IOCs" during blocking.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Remediation Action|Specify the remediation action for the entities.|False|List|Block and Delete|
|Description|Specify a description that should be added to the blocked entities.|True|String|Blocked by Siemplify|



##### JSON Results
```json
[{"Entity": "172.30.xxx.xx", "EntityResult": {"status": "Failure", "reason": "Invalid value"}}, {"Entity": "url.com", "EntityResult": {"status": "Success"}}]
```



#### Ping
Test connectivity to the Symantec Email Security.Cloud with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









