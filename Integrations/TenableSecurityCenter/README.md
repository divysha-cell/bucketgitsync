
# TenableSecurityCenter

SecurityCenter is a comprehensive vulnerability analysis solution that provides complete visibility into the security posture of your distributed and complex IT infrastructure. 

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|The server Address of the Tenable Security Center.|True|IP|None|
|Username|The username of the Tenable Security Center account. Note: Both “Username” and “Password” must be provided.|False|String|None|
|Password|The password of the Tenable Security Center account. Note: Both “Username” and “Password” must be provided.|False|Password|*****|
|Access Key|The Access Key of the Tenable Security Center account. Note: Both “Access Key” and “Secret Key” must be provided.|False|Password|*****|
|Secret Key|The Secret Key of the Tenable Security Center account. Note: Both “Access Key” and “Secret Key” must be provided.|False|Password|*****|
|Use SSL|If selected, the integration validates the SSL certificate when connecting to the Tenable Security Center server. Enabled by default.|False|Boolean|False|


#### Dependencies
| |
|-|
|tzdata-2026.2-py2.py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|arrow-1.4.0-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-1.26.20-py2.py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Get Vulnerabilities for IP
Get vulnerabilities and severity summary for an IP address
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": [{"macAddress": "", "protocol": "TCP", "uuid": "", "family": "Web Servers", "pluginInfo": "10107 (443/6) HTTP Server Type and Version", "ip": "1.1.1.1", "pluginID": "10107", "severity": "Info", "repository": "repo", "uniqueness": "repositoryID,ip,dnsName", "dnsName": "google-public-dns-a.google.com", "port": "443", "netbiosName": "", "name": "HTTP Server Type and Version"}, {"macAddress": "", "protocol": "UDP", "uuid": "", "family": "DNS", "pluginInfo": "10539 (53/17) DNS Server Recursive Query Cache Poisoning Weakness", "ip": "1.1.1.1", "pluginID": "10539", "severity": "Medium", "repository": "repo", "uniqueness": "repositoryID,ip,dnsName", "dnsName": "google-public-dns-a.google.com", "port": "53", "netbiosName": "", "name": "DNS Server Recursive Query Cache Poisoning Weakness"}, {"macAddress": "", "protocol": "TCP", "uuid": "", "family": "General", "pluginInfo": "10863 (443/6) SSL Certificate Information", "ip": "1.1.1.1", "pluginID": "10863", "severity": "Info", "repository": "repo", "uniqueness": "repositoryID,ip,dnsName", "dnsName": "google-public-dns-a.google.com", "port": "443", "netbiosName": "", "name": "SSL Certificate Information"}], "Entity": "1.1.1.1"}]
```



#### Scan Ips
Initiate a scan of IP addresses
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Name|The name of the scan to create.|True|String||
|Policy Name|The name of the policy.|True|String||



#### Get Report
Get report content by ID or name.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report ID|Report ID number.Can be found at the report URL.|False|String|None|
|Report Name|The name of the report, as mentioned at the GUI.|False|String|None|



##### JSON Results
```json
{"pubSites": ["https://test.com", "https://test.test"]}
```



#### Get Scan Results
Wait for scan to complete and get results of the scan
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Result ID|The scan results ID.|True|String||



##### JSON Results
```json
{"severity_summary": [{"count": "0", "severity": {"id": "4", "name": "Critical", "description": "Critical Severity"}}, {"count": "0", "severity": {"id": "3", "name": "High", "description": "High Severity"}}, {"count": "3", "severity": {"id": "2", "name": "Medium", "description": "Medium Severity"}}], "results": [{"name": "DNS Server Recursive Query Cache Poisoning Weakness", "family": "DNS", "hostTotal": "1", "pluginID": "10539", "total": "1", "severity": "Medium"}, {"name": "DNS Server Spoofed Request Amplification DDoS", "family": "DNS", "hostTotal": "1", "pluginID": "35450", "total": "1", "severity": "Medium"}, {"name": "SSL Medium Strength Cipher Suites Supported", "family": "General", "hostTotal": "1", "pluginID": "42873", "total": "1", "severity": "Medium"}]}
```



#### Run Asset Scan
Execute Asset Scan in Tenable.sc.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Name|Specify the name for the scan.|True|String||
|Asset Name|Specify the name of the asset that should be scanned.|True|String||
|Policy ID|Specify the id of the policy that should be used in the scan.|True|String||
|Repository ID|Specify the id of the repository that should be used in the scan.|True|String||
|Description|Specify the description for the scan.|False|String||



##### JSON Results
```json
{"emailOnLaunch": "false", "creator": {"username": "example_username", "lastname": "Security", "id": "xxx", "firstname": "Manager"}, "numDependents": "0", "maxScanTime": "3600", "dhcpTracking": "false", "ipList": "", "owner": {"username": "example_username", "lastname": "Security", "id": "xxx", "firstname": "Manager"}, "id": "xxx", "scanningVirtualHosts": "false", "canUse": "true", "timeoutAction": "import", "zone": {"description": "", "id": "xxx", "name": ""}, "schedule": {"repeatRule": "", "dependent": {"description": "", "id": "xxx", "name": ""}, "enabled": "true", "nextRun": -1, "start": "", "type": "now", "id": "xxx", "objectType": -1}, "classifyMitigatedAge": "0", "rolloverType": "template", "policy": {"description": "", "tags": "", "ownerGroup": {"description": "Full Access group", "id": "xxx", "name": "Full Access"}, "context": "", "owner": {"username": "example_username", "lastname": "Security", "id": "xxx", "firstname": "Manager"}, "id": "100xxxx", "name": "Host Discovery"}, "type": "policy", "status": "0", "canManage": "true", "description": "test test", "modifiedTime": "1607591645", "emailOnFinish": "false", "ownerGroup": {"description": "Full Access group", "id": "xxx", "name": "Full Access"}, "policyPrefs": [{"name": "MODE|discovery", "value": "host_enumeration"}, {"name": "description", "value": ""}, {"name": "display_unreachable_hosts", "value": "no"}, {"name": "log_live_hosts", "value": "yes"}, {"name": "name", "value": "Host Discovery"}, {"name": "reverse_lookup", "value": "no"}], "credentials": [], "name": "test", "assets": [{"description": "", "id": "xxx", "name": "test"}], "plugin": {"description": "", "id": "xxx", "name": ""}, "reports": [], "repository": {"description": "", "id": "xxx", "name": "test"}, "createdTime": "1607591645", "scanResultID": "xxx"}
```



#### Get Related Assets
Get assets that are related to an IP address
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Repository Name|The repository name.|True|String||



##### JSON Results
```json
[{"EntityResult": [{"id": "0", "description": "All defining ranges of the Group in whose context this Asset is being evaluated.", "name": "All Defined Ranges"}, {"id": "2", "description": "This asset uses the Scan Summary plugin to detect if a host has been scanned by Nessus. The Scan Summary plugin contains the list of tests conducted during the most recent scan.", "name": "Systems that have been Scanned"}, {"id": "13", "description": "Leverage Nessus plugin 10180 (Ping the remote host) and Nessus plugin 12503 (Host Fully Qualified Domain Name (FQDN) Resolution) to find hosts that don't have a resolvable FQDN in DNS.", "name": "Scanned Hosts Not in DNS"}], "Entity": "1.1.1.1"}]
```



#### Add IP To IP List Asset
Add an IP to IP list asset in Tenable.sc.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Asset Name|Specify the name of the IP list asset to which you want to add new IPs.|True|String||



##### JSON Results
```json
{"creator": {"username": "security_manager", "lastname": "Security", "id": "1", "firstname": "Manager"}, "typeFields": {"definedIPs": "88.203.xxx.xxx"}, "ioLastSyncSuccess": "-1", "owner": {"username": "security_manager", "lastname": "Security", "id": "1", "firstname": "Manager"}, "targetGroup": {"description": "", "id": -1, "name": ""}, "id": "xx", "canUse": "true", "ioFirstSyncTime": "-1", "template": {"description": "", "id": -1, "name": ""}, "ioSyncStatus": "Not Synced", "type": "static", "status": "0", "canManage": "true", "description": "Asset description", "modifiedTime": "1607603911", "tags": "My Tag", "ioSyncErrorDetails": null, "ownerGroup": {"description": "Full Access group", "id": "0", "name": "Full Access"}, "createdTime": "1607603911", "groups": [], "ipCount": -1, "name": "Test2", "repositories": [{"repository": {"description": "", "id": "1", "name": "Siemplify-Repo"}, "ipCount": "-1"}], "context": "", "assetDataFields": [], "ioLastSyncFailure": "-1"}
```



#### Create IP List Asset
Create an IP list asset in Tenable.sc. Requires at least 1 IP entity for successful execution.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name for the IP list asset.|True|String||
|Description|Specify the description of the IP list asset.|False|String||
|Tag|Specify the tag of the IP list asset.|False|String||



##### JSON Results
```json
{"creator": {"username": "security_manager", "lastname": "Security", "id": "1", "firstname": "Manager"}, "typeFields": {"definedIPs": "88.203.xxx.xxx"}, "ioLastSyncSuccess": "-1", "owner": {"username": "security_manager", "lastname": "Security", "id": "1", "firstname": "Manager"}, "targetGroup": {"description": "", "id": -1, "name": ""}, "id": "xx", "canUse": "true", "ioFirstSyncTime": "-1", "template": {"description": "", "id": -1, "name": ""}, "ioSyncStatus": "Not Synced", "type": "static", "status": "0", "canManage": "true", "description": "Asset description", "modifiedTime": "1607603911", "tags": "My Tag", "ioSyncErrorDetails": null, "ownerGroup": {"description": "Full Access group", "id": "0", "name": "Full Access"}, "createdTime": "1607603911", "groups": [], "ipCount": -1, "name": "Test2", "repositories": [{"repository": {"description": "", "id": "1", "name": "Siemplify-Repo"}, "ipCount": "-1"}], "context": "", "assetDataFields": [], "ioLastSyncFailure": "-1"}
```



#### Enrich IP
Get information about IP addresses and enrich them
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Repository Name|The repository name.|True|String||



##### JSON Results
```json
[{"EntityResult": {"macAddress": "", "severityLow": "0", "links": [], "ip": "1.1.1.1", "lastScan": "1549425224", "severityCritical": "0", "total": "2", "severityAll": "0,0,0,0,2", "mcafeeGUID": "", "policyName": "1e2e4247-0de7-56d5-8026-34ab1f3150ef-1130313/Basic Discovery Scan", "uuid": "", "lastAuthRun": "", "severityInfo": "2", "keyDrivers": "", "hostUniqueness": "repositoryID", "assetExposureScore": "", "hostUUID": "", "acrScore": "", "osCPE": "", "uniqueness": "repositoryID,ip,dnsName", "dnsName": "google-public-dns-a.google.com", "repository": {"id": "1", "description": "", "name": "repo", "uuid": "", "type": "Local"}, "lastUnauthRun": "1549363419", "biosGUID": "", "tpmID": "", "score": "0", "hasPassive": "No", "pluginSet": "201902020242", "hasCompliance": "No", "severityHigh": "0", "netbiosName": "", "severityMedium": "0", "os": ""}, "Entity": "1.1.1.1"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









## Connectors
#### Tenable Security Center Connector
Tenable Security Center Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|Server Address|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|
|Access Key|Access Key|False|Password|*****|
|Secret Key|Secret Key|False|Password|*****|
|Use SSL|Use SSL|False|Boolean|FALSE|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Max Days Backwards|Specify the amount of days back, from which you would like to fetch data.|False|String|1|
|Limit Per Cycle|Specify the amount of alerts ingested into the connector in each execution cycle.|False|String|10|




