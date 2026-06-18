
# Zscaler

Zscaler is a cloud security solution built for performance and flexible scalability. Use the Zscaler integration to block and manage domains using whitelists and blacklists.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|The base URL of the Zscaler instance.|True|String|https://admin.zscalertwo.net|
|Login ID|The username or email address associated with the Zscaler administrator account used for authentication. This parameter is mandatory for legacy authentication. If both legacy and OAuth 2.0 credentials are provided, OAuth 2.0 takes precedence.|False|String||
|Api Key|The unique API key generated in the Zscaler portal to authorize API requests. This parameter is mandatory for legacy authentication. If both legacy and OAuth 2.0 credentials are provided, OAuth 2.0 takes precedence.|False|Password|*****|
|Password|The password associated with the Zscaler administrator account used for authentication. This parameter is mandatory for legacy authentication. If both legacy and OAuth 2.0 credentials are provided, OAuth 2.0 takes precedence.|False|Password|*****|
|Client ID|The unique identifier for the OAuth 2.0 client used for authentication using the ZSLogin service. This parameter is mandatory for OAuth 2.0 configuration and takes precedence over legacy authentication.|False|String||
|Client Secret|The secret key associated with the client ID used to authenticate the OAuth 2.0 client. This parameter is mandatory for OAuth 2.0 configuration and takes precedence over legacy authentication.|False|Password|*****|
|Login API Root|The base URL for the ZSLogin service used for centralized identity and access management. This parameter is mandatory for OAuth 2.0 configuration and takes precedence over legacy authentication.|False|String|https://siempify.zslogin.net|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to the Zscaler server.|False|Boolean|False|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|proto_plus-1.27.2-py3-none-any.whl|
|TIPCommon-2.3.4-py3-none-any.whl|
|protobuf-6.33.6-cp39-abi3-manylinux2014_x86_64.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|charset_normalizer-3.4.6-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|httpx-0.28.1-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|google_api_core-2.30.1-py3-none-any.whl|
|cryptography-46.0.6-cp311-abi3-manylinux_2_34_x86_64.whl|
|googleapis_common_protos-1.73.1-py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|


## Actions
#### Add To Blacklist
Adds a URL/Domain/IP to black list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOCs|A comma-separated list of IOCs (IP Addresses, URLs, or Domains) to add to the blacklist. Example: "10.1.1.1, google.com, http://badsite.net"|False|String||



#### Get Sandbox Report
Get a full report for an MD5 hash of a file that was analyzed by Sandbox.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"Full Details": {"SystemSummary": [{"SignatureSources": ["", "76CD0000 page execute and read and write", "76DD0000 page execute and read and write"], "Risk": "LOW", "Signature": "Allocates memory within range which is reserved for system DLLs"}, {"SignatureSources": ["", "wow64.pdb source: loaddll32.exe", "wow64.pdbH source: loaddll32.exe", "wow64cpu.pdb source: loaddll32.exe", "wow64win.pdb source: loaddll32.exe", "wow64win.pdbH source: loaddll32.exe"], "Risk": "LOW", "Signature": "Binary contains paths to debug symbols"}, {"SignatureSources": ["", "clean0.winDLL@1/1@0/0"], "Risk": "LOW", "Signature": "Classification label"}, {"SignatureSources": ["", "More than 502 > 100 exports found"], "Risk": "LOW", "Signature": "PE file exports many functions"}, {"SignatureSources": ["", "Virtual size of .text is bigger than: 0x100000"], "Risk": "LOW", "Signature": "PE file has a big code size"}, {"SignatureSources": ["", "Raw size of .text is bigger than: 0x100000 < 0x176000"], "Risk": "LOW", "Signature": "PE file has a big raw section"}, {"SignatureSources": ["", "Image base 0x704c0000 > 0x60000000"], "Risk": "LOW", "Signature": "PE file has a high image base. often used for DLLs"}, {"SignatureSources": ["", "Section: .text IMAGE_SCN_ALIGN_MASK, IMAGE_SCN_ALIGN_256BYTES, IMAGE_SCN_ALIGN_16BYTES, IMAGE_SCN_ALIGN_64BYTES, IMAGE_SCN_ALIGN_1BYTES, IMAGE_SCN_MEM_EXECUTE, IMAGE_SCN_CNT_INITIALIZED_DATA, IMAGE_SCN_ALIGN_2048BYTES, IMAGE_SCN_ALIGN_1024BYTES, IMAGE_SCN"], "Risk": "LOW", "Signature": "PE file has an executable .text section and no other executable section"}, {"SignatureSources": ["", "HKEY_USERS\\Software\\Policies\\Microsoft\\Windows\\Safer\\CodeIdentifiers"], "Risk": "LOW", "Signature": "Reads software policies"}, {"SignatureSources": ["", "File size 1710606 > 1048576"], "Risk": "LOW", "Signature": "Submission file is bigger than most known malware samples"}, {"SignatureSources": ["", "no activity detected"], "Risk": "MODERATE", "Signature": "Program does not show much activity"}], "Summary": {"Status": "COMPLETED", "Category": "EXECS", "FileType": "DLL", "Duration": 499618, "StartTime": 1553130306}, "Classification": {"Category": "BENIGN", "Type": "BENIGN", "Score": 0, "DetectedMalware": ""}, "Persistence": [{"SignatureSources": ["", "section name: /4"], "Risk": "LOW", "Signature": "PE file contains sections with non-standard names"}], "FileProperties": {"SHA1": "b0aa7eecfa6c0066504bf79efe1bc057ac61e9b8", "FileSize": 1710606, "RootCA": "", "Issuer": "", "FileType": "DLL", "Sha256": "a39180232ae6a689650f5df566bb4e81b94d9d19a53363ce17d7a12fd21f78cf", "DigitalCerificate": "", "SSDeep": "24576:3LnYQhDtnNgQe42lcCZNj4I/MmaOdb+Y+mmY5Gc3nGkh2sQginrgGGQCTQIMGNdd:zYQlEpIE/p3nFhckZF7oU", "MD5": "1803c2c0f0ec61c98b3630d7e4b1cd5d"}}}, "Entity": "1803C2C0F0EC61C98B3630D7E4B1CD5D"}]
```



#### Get Blacklist
Gets a list of black-listed URLs.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Add To Whitelist
Adds a URL/Domain/IP to the white-listed URLs. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOCs|A comma-separated list of IOCs (IP Addresses, URLs, or Domains) to add to the whitelist. Example: "10.1.1.1, google.com, http://badsite.net"|False|String||



#### Get Url Categories
Gets information about all URL categories.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Display URL|True to display URLs of each category, otherwise false.|False|Boolean|False|



##### JSON Results
```json
[{"description": "OTHER_ADULT_MATERIAL_DESC", "val": 1, "dbCategorizedUrls": [], "editable": true, "urls": [], "customCategory": false, "id": "OTHER_ADULT_MATERIAL"}, {"description": "ADULT_THEMES_DESC", "val": 2, "dbCategorizedUrls": [], "editable": true, "urls": [], "customCategory": false, "id": "ADULT_THEMES"}]
```



#### Get Whitelist
Gets a list of white-listed URLs.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Lookup Entity
Look up the categorization of a URL/Domain/IP
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"url": "someurl1.com/f1q7qx.php", "urlClassificationsWithSecurityAlert": ["MALWARE_SITE"], "urlClassifications": []}, "Entity": "HTTP://SOMEURL1.COM/F1Q7QX.PHP"}]
```



#### Ping
Check connectivity
Timeout - 600 Seconds



#### Remove From Blacklist
Removes a URL/Domain/IP from the black list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOCs|A comma-separated list of IOCs (IP Addresses, URLs, or Domains) to remove from the blacklist. Example: "10.1.1.1, google.com, http://badsite.net"|False|String||



#### Remove From Whitelist
Removes a URL/Domain/IP from the white-listed URLs
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOCs|A comma-separated list of IOCs (IP Addresses, URLs, or Domains) to remove from the whitelist. Example: "10.1.1.1, google.com, http://badsite.net"|False|String||









