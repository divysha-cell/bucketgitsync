
# VirusTotal

VirusTotal is a service that analyzes files and URLs for viruses, worms, trojans and other kinds of malicious content. VirusTotal aggregates many antivirus products and online scan engines to check for viruses that the user's own antivirus may have missed, or to verify against any false positives. Use VirusTotal to investigate suspicious files, domains, URLs, IP addresses, and hashes.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key|None|True|Password||
|Verify SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|paramiko-3.4.0-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|asn1crypto-1.5.1-py2.py3-none-any.whl|
|cffi-1.16.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.2.1-py3-none-any.whl|
|PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl|
|idna-3.6-py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|bcrypt-4.1.3-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cryptography-42.0.5-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|requests-2.31.0-py3-none-any.whl|


## Actions
#### Get Domain Report
Scan Domain via VirusTotal. *Check online report for full details.
Timeout - 600 Seconds



#### Upload And Scan Files
Upload and scan files via VirusTotal. *Files can be uploaded from remote path (Windows share or Linux remote server).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Entity risk threshold.|True|None||
|File Paths|Target file path.|True|None||
|Linux Server Address|Linux server address(e.g: x.x.x.x).|False|None||
|Linux User|Linux User|False|None||
|Linux Password|Linux Password|False|None||



#### Scan URL
Scan URL via VirusTotal. *Mark entity as suspicious and show insights if risk score matches a given threshold.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if number of negative engines is equal or above the given threshold|True|None||
|Rescan after days|Action will fetch the latest result. If the result is older than mentioned days it will automatically rescan the entity|False|None||



#### Scan IP
Scan IP via VirusTotal. Returns table of reverse domains and full Json result
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Specify the accepted threshold for the detected samples related to the IP address. If the number of engines that marked related samples as malicious is higher than the specified threshold, IP address will be marked as suspicious.|False|None||



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Scan Hash
Scan Hash via VirusTotal. *Mark entity as suspicious and show insights if risk score matches a given threshold.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if number of negative engines is equal or above the given threshold|True|None||
|Rescan after days|Action will fetch the latest result. If the result is older than mentioned days it will automatically rescan the entity|False|None||









