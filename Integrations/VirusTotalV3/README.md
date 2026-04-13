
# VirusTotalV3

VirusTotal was founded in 2004 as a free service that analyzes files and URLs for viruses, worms, trojans and other kinds of malicious content. Our goal is to make the internet a safer place through collaboration between members of the antivirus industry, researchers and end users of all kinds. Fortune 500 companies, governments and leading security companies are all part of the VirusTotal community, which has grown to over 500,000 registered users.This integration was created using the 3rd iteration of VT API.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|None|True|Password||
|Verify SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|proto_plus-1.25.0-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|cryptography-43.0.1-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|anyio-4.6.2.post1-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|tldextract-5.1.3-py3-none-any.whl|
|google_auth-2.36.0-py2.py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|paramiko-3.5.0-py3-none-any.whl|
|TIPCommon-2.0.6-py2.py3-none-any.whl|
|httpcore-1.0.6-py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|google_api_core-2.23.0-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|filelock-3.16.1-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|google_api_python_client-2.151.0-py2.py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|bcrypt-4.2.0-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Add Vote To Entity
Add a vote to entities in VirusTotal. Supported entities: File Hash, URL, Hostname, Domain, IP Address. Note: only MD5, SHA-1 and SHA-256 Hash types are supported
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vote|Specify the vote that should be added to entities.|True|None||



#### Enrich Hash
Enrich Hash using information from VirusTotal. Supported entities: Filehash. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Engine Threshold|Specify how many engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count results from those engines.|False|None||
|Engine Percentage Threshold|Specify the percentage of engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count the percentage from those engines. If both "Engine Threshold" and "Engine Percentage Threshold" are provided, "Engine Threshold" will be used. Maximum value: 100. Minimum: 0.|False|None||
|Engine Whitelist|Specify a comma-separated list of engines that should be used to retrieve information, whether an entity is malicious or not. Example: AlienVault,Kaspersky. Note: if nothing is specified in this parameter, action will take results from every available engine. If the engine didn't return any information about the entity it’s not going to be counted for the parameters "Engine Threshold" and "Engine Percentage Threshold".|False|None||
|Resubmit Hash|If enabled, action will resubmit hashes for analysis instead of using the latest information.|False|None||
|Resubmit After (Days)|Specify how many days since the last submission should pass for the entity to be submitted again. Note: parameter "Resubmit Hash" needs to be enabled.|False|None||
|Retrieve Comments|If enabled, action will retrieve comments about the entity.|False|None||
|Retrieve Sigma Analysis|If enabled, action will retrieve sigma analysis for the hash.|False|None||
|Sandbox|Specify a comma-separated list of sandbox names that should be used for behavior analysis. If nothing is provided, action will only use the "VirusTotal Jujubox" sandbox. Make sure that the spelling is correct. Examples of sandboxes: VirusTotal Jujubox, VirusTotal ZenBox, Microsoft Sysinternals, Tencent HABO.|False|None||
|Retrieve Sandbox Analysis|If enabled, action will fetch sandbox analysis for the entity. For each sandbox, action will create a separate section in the JSON result. Action will only return data for the sandboxes that are provided in the parameter "Sandbox".|False|None||
|Create Insight|If enabled, action will create an insight containing information about the entities.|False|None||
|Only Suspicious Entity Insight|If enabled, action will only create an insight for suspicious entities. Note: parameter "Create Insight" should be enabled.|False|None||
|Max Comments To Return|Specify how many comments to return. Default: 10.|False|None||
|Widget Theme|Specify the theme for the widget.|False|None||
|Fetch Widget|If enabled, action will fetch augmented widget related to the entity.|False|None||
|Fetch MITRE Details|If enabled, action will return information about related MITRE techniques and tactics.|False|None||
|Lowest MITRE Technique Severity|Specify the lowest signature severity related to MITRE technique for technique to be returned. "Unknown" severity is treated as "Info".|False|None||



#### Get Related Hashes
Get related hashes to the provided entities from VirusTotal. Note: this action requires a VT Enterprise token. Supported entities: IP, URL, Filehash, Hostname, Domain. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Results|Specify how the JSON result should look like. If "Combined" is selected then action will return all of the unique results that were found among the provided entities. If "Per Entity" is selected, then action will return all of the unique items per entity.|False|None||
|Max Hashes To Return|Specify how many URLs to return. Depending on the parameter "Results", this parameter will behave differently. For "Combined" the limit will define how many results to return from ALL entities. For "Per Entity" this parameter dictates how many results to return per entity. Default: 40.|False|None||



#### Get Related Domains
Get related domains to the provided entities from VirusTotal. Note: this action requires a VT Enterprise token. Supported entities: IP, URL, Filehash, Hostname, Domain. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Results|Specify how the JSON result should look like. If "Combined" is selected then action will return all of the unique results that were found among the provided entities. If "Per Entity" is selected, then action will return all of the unique items per entity.|False|None||
|Max Domains To Return|Specify how many URLs to return. Depending on the parameter "Results", this parameter will behave differently. For "Combined" the limit will define how many results to return from ALL entities. For "Per Entity" this parameter dictates how many results to return per entity. Default: 40.|False|None||



#### Ping
Test connectivity to the VirusTotal with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Get Related URLs
Get related urls to the provided entities from VirusTotal. Note: this action requires a VT Enterprise token. Supported entities: IP, URL, Filehash, Hostname, Domain. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Results|Specify how the JSON  result should look like. If "Combined" is selected then action will return all of the unique results that were found among the provided entities. If "Per Entity" is selected, then action will return all of the unique items per entity.|False|None||
|Max URLs To Return|Specify how many URLs to return. Depending on the parameter "Results", this parameter will behave differently. For "Combined" the limit will define how many results to return from ALL entities. For "Per Entity" this parameter dictates how many results to return per entity. Default: 40.|False|None||



#### Add Comment To Entity
Add a comment to entities in VirusTotal. Supported entities: File Hash, URL, Hostname, Domain, IP Address. Note: only MD5, SHA-1 and SHA-256 Hash types are supported
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Comment|Specify the comment that should be added to entities.|True|None||



#### Search Graphs
Search graphs based on custom filters in VirusTotal.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query filter for the graph. Please refer to the documentation portal for more details.|True|None||
|Sort Field|Specify what should be the sort field.|False|None||
|Max Graphs To Return|Specify how many graphs to return.|False|None||



#### Search IOCs
Search for IOCs in the VirusTotal's dataset, using the same query syntax that you would use in the VirusTotal Intelligence user interface. This action requires a VT Enterprise token.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query according to the VirusTotal query search syntax.|True|None||
|Create Entities|If enabled, action will create entities for the returned IOCs. Note: this action does not enrich entities.|False|None||
|Order By|Specify the order by the selected field, in which results are returned. Default: Use Default Order. Note: Entity types might have different ordering fields. Refer to the VT Intelligence corpus https://docs.virustotal.com/reference/intelligence-search for more information.|True|None||
|Sort Order|Specify the direction in which the results should be returned. If “Use Default Order” is chosen for “Order By” field, this parameter will be ignored.|False|None||
|Max IOCs To Return|Specify how many IOCs to return. Max IOCs to return is 300. Default: 10.|False|None||



#### Submit File
Submit a file and return results from VirusTotal.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|Specify a comma-separated list of absolute file paths. Note: if "Linux Server Address" is specified, action will try to fetch file from remote server.|True|None||
|Engine Threshold|Specify how many engines should mark the file as malicious or suspicious, for Siemplify to label it as risky. Note: if "Engine Whitelist" contains values, action will only count results from those engines. If the submission is done privately, action will mark the entity as suspicious based on the verdict of API without counting the engines.|False|None||
|Engine Percentage Threshold|Specify the percentage of engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count the percentage from those engines. If both "Engine Threshold" and "Engine Percentage Threshold" are provided, "Engine Threshold" will be used. Maximum value: 100. Minimum: 0.|False|None||
|Engine Whitelist|Specify a comma-separated list of engines that should be used to retrieve information, whether an entity is malicious or not. Example: AlienVault,Kaspersky. Note: if nothing is specified in this parameter, action will take results from every available engine. If the engine didn't return any information about the entity it’s not going to be counted for the parameters "Engine Threshold" and "Engine Percentage Threshold".|False|None||
|Retrieve Comments|If enabled, action will retrieve comments about the entity.|False|None||
|Max Comments To Return|Specify how many comments to return.|False|None||
|Linux Server Address|Specify the IP address of the remote linux server, where the file is located.|False|None||
|Linux Username|Specify the username of the remote linux server, where the file is located.|False|None||
|Linux Password|Specify the password of the remote linux server, where the file is located.|False|None||
|Private Submission|If enabled, action will submit the file privately. Note: this functionality requires premium VT access.|False|None||
|Fetch MITRE Details|If enabled, action will return information about related MITRE techniques and tactics.|False|None||
|Lowest MITRE Technique Severity|Specify the lowest signature severity related to MITRE technique for technique to be returned. "Unknown" severity is treated as "Info".|False|None||
|Retrieve AI Summary|Experimental. If enabled, action will retrieve an AI Summary for the submitted file. AI Summary is only available for private submissions.|False|None||



#### Get Domain Details
Get detailed information about the domain using information from VirusTotal. Supported entities: URL (entity extracts domain part), Hostname, Domain.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Engine Threshold|Specify how many engines should mark the domain as malicious or suspicious, for Siemplify to label it as risky. Note: if "Engine Whitelist" contains values, action will only count results from those engines.|False|None||
|Engine Percentage Threshold|Specify the percentage of engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count the percentage from those engines. If both "Engine Threshold" and "Engine Percentage Threshold" are provided, "Engine Threshold" will be used. Maximum value: 100. Minimum: 0.|False|None||
|Engine Whitelist|Specify a comma-separated list of engines that should be used to retrieve information, whether an entity is malicious or not. Example: AlienVault,Kaspersky. Note: if nothing is specified in this parameter, action will take results from every available engine. If the engine didn't return any information about the entity it’s not going to be counted for the parameters "Engine Threshold" and "Engine Percentage Threshold".|False|None||
|Retrieve Comments|If enabled, action will retrieve comments about the entity.|False|None||
|Create Insight|If enabled, action will create an insight containing information about the entities.|False|None||
|Only Suspicious Entity Insight|If enabled, action will only create an insight for suspicious entities. Note: parameter "Create Insight" should be enabled.|False|None||
|Max Comments To Return|Specify how many comments to return. Default: 10.|False|None||
|Widget Theme|Specify the theme for the widget.|False|None||
|Fetch Widget|If enabled, action will fetch augmented widget related to the entity.|False|None||



#### Download File
Download file from VirusTotal. Supported entities: Filehash. Note: this action requires a VT Enterprise token. Only MD5, SHA-1, SHA-256 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Download Folder Path|Specify the path to the folder, where you want to store the files.|True|None||
|Overwrite|If enabled, action will overwrite the file with the same name.|False|None||



#### Get Graph Details
Get detailed information about graphs in VirusTotal.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Graph ID|Specify a comma-separated list of graph ids for which you want to retrieve detailed information.|True|None||
|Max Links To Return|Specify how many links to return.|False|None||



#### Enrich URL
Enrich URL using information from VirusTotal. Supported entities: URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Engine Threshold|Specify how many engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count results from those engines.|False|None||
|Engine Percentage Threshold|Specify the percentage of engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count the percentage from those engines. If both "Engine Threshold" and "Engine Percentage Threshold" are provided, "Engine Threshold" will be used. Maximum value: 100. Minimum: 0.|False|None||
|Engine Whitelist|Specify a comma-separated list of engines that should be used to retrieve information, whether an entity is malicious or not. Example: AlienVault,Kaspersky. Note: if nothing is specified in this parameter, action will take results from every available engine. If the engine didn't return any information about the entity it’s not going to be counted for the parameters "Engine Threshold" and "Engine Percentage Threshold".|False|None||
|Resubmit URL|If enabled, action will resubmit urls for analysis instead of using the latest information.|False|None||
|Retrieve Comments|If enabled, action will retrieve comments about the entity.|False|None||
|Only Suspicious Entity Insight|If enabled, action will only create an insight for suspicious entities. Note: parameter "Create Insight" should be enabled.|False|None||
|Create Insight|If enabled, action will create an insight containing information about the entities.|False|None||
|Max Comments To Return|Specify how many comments to return. Default: 10.|False|None||
|Resubmit After (Days)|Specify how many days since the last submission should pass for the entity to be submitted again. Note: parameter "Resubmit URL" needs to be enabled. Default: 30.|False|None||
|Widget Theme|Specify the theme for the widget.|False|None||
|Fetch Widget|If enabled, action will fetch augmented widget related to the entity.|False|None||



#### Enrich IOC
Enrich IOCs using information from VirusTotal.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOC Type|Specify the type of the IOC.|False|None||
|IOCs|Specify a comma-separated list of IOCs for which you want to ingest data.|True|None||
|Widget Theme|Specify the theme for the widget.|False|None||
|Fetch Widget|If enabled, action will fetch augmented widget related to the entity.|False|None||



#### Enrich IP
Enrich IP using information from VirusTotal. Supported entities: IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Engine Threshold|Specify how many engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count results from those engines.|False|None||
|Engine Percentage Threshold|Specify the percentage of engines should mark the entity as malicious or suspicious, for Siemplify to label it as suspicious. Note: if "Engine Whitelist" contains values, action will only count the percentage from those engines. If both "Engine Threshold" and "Engine Percentage Threshold" are provided, "Engine Threshold" will be used. Maximum value: 100. Minimum: 0.|False|None||
|Engine Whitelist|Specify a comma-separated list of engines that should be used to retrieve information, whether an entity is malicious or not. Example: AlienVault,Kaspersky. Note: if nothing is specified in this parameter, action will take results from every available engine. If the engine didn't return any information about the entity it’s not going to be counted for the parameters "Engine Threshold" and "Engine Percentage Threshold".|False|None||
|Retrieve Comments|If enabled, action will retrieve comments about the entity.|False|None||
|Create Insight|If enabled, action will create an insight containing information about the entities.|False|None||
|Only Suspicious Entity Insight|If enabled, action will only create an insight for suspicious entities. Note: parameter "Create Insight" should be enabled.|False|None||
|Max Comments To Return|Specify how many comments to return. Default: 10|False|None||
|Widget Theme|Specify the theme for the widget.|False|None||
|Fetch Widget|If enabled, action will fetch augmented widget related to the entity.|False|None||



#### Get Related IPs
Get related IPs to the provided entities from VirusTotal. Note: this action requires a VT Enterprise token. Supported entities: URL, Filehash, Hostname, Domain. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Results|Specify how the JSON result should look like. If "Combined" is selected then action will return all of the unique results that were found among the provided entities. If "Per Entity" is selected, then action will return all of the unique items per entity.|False|None||
|Max IPs To Return|Specify how many URLs to return. Depending on the parameter "Results", this parameter will behave differently. For "Combined" the limit will define how many results to return from ALL entities. For "Per Entity" this parameter dictates how many results to return per entity. Default: 40.|False|None||



#### Search Entity Graphs
Search graphs based on the entities in VirusTotal. Supported entities: IP, URL, Filehash, Hostname, Domain, Threat Actor, User. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sort Field|Specify what should be the sort field.|False|None||
|Max Graphs To Return|Specify how many graphs to return.|False|None||









## Connectors
#### VirusTotal - Livehunt Notifications Connector
Pull information about Livehunt notifications and related files from VirusTotal. Note: this connector requires a premium API token. Dynamic list works with "rule_name" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|None||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|None|.*|
|API Key|VirusTotal API Key.|True|None||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the VirusTotal server is valid.|False|None|true|
|Engine Whitelist|Specify a comma-separated list of engines that should be used, when counting the \'Engine Percentage Threshold To Fetch\' parameter. Example: AlienVault,Kaspersky. Note: if nothing is provided, all engines from the response are counted.|False|None||
|Engine Percentage Threshold To Fetch|The percentage of engines that need to mark the file as suspicious/malicious before it's being ingested. Maximum value: 100. Minimum: 0.|True|None|0|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve notifications from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|None|1|
|Max Notifications To Fetch|How many notifications to process per one connector iteration. Default: 40.|False|None|40|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|None|false|
|Proxy Server Address|The address of the proxy server to use.|False|None||
|Proxy Username|The proxy username to authenticate with.|False|None||
|Proxy Password|The proxy password to authenticate with.|False|None||




