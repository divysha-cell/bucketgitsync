
# TenableIO

Managed in the cloud and powered by Nessus technology, Tenable.io provides the industry's most comprehensive vulnerability coverage with the ability to predict which security issues to remediate first. It’s your complete end-to-end vulnerability management solution.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://cloud.tenable.com|
|Secret Key|None|True|Password|*****|
|Access Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|idna-3.8-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|


## Actions
#### List Plugin Families
List available plugin families from Tenable.io.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among record types and if “Contains“ is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Plugin Families To Return|Specify how many plugin families to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"count":11396,"name":"AIX Local Security Checks","id":27},{"count":2008,"name":"Amazon Linux Local Security Checks","id":28},{"count":121,"name":"Backdoors","id":9}]
```



#### List Endpoint Vulnerabilities
List endpoint vulnerabilities in Tenable.io. Supported entities: IP Address, Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Lowest Severity To Fetch|Specify the lowest severity that will be used to fetch vulnerabilities.|False|List|Info|
|Max Vulnerabilities To Return|Specify how many vulnerabilities to return per entity. Default: 50. Maximum: 200.|False|String|50|



##### JSON Results
```json
[{"Entity":"Hostname","EntityResult":[{"count":1,"plugin_family":"Windows","plugin_id":103569,"plugin_name":"Windows Defender Antimalware/Antivirus Signature Definition Check","vulnerability_state":"Active","accepted_count":0,"recasted_count":0,"counts_by_severity":[{"count":1,"value":3}],"severity":3},{"count":1,"plugin_family":"Windows : Microsoft Bulletins","plugin_id":131025,"plugin_name":"Security Updates for Exchange (November 2019)","vulnerability_state":"Active","vpr_score":6.7,"accepted_count":0,"recasted_count":0,"counts_by_severity":[{"count":1,"value":3}],"cvss_base_score":7.5,"cvss3_base_score":9.8,"severity":3}]}]
```



#### Enrich Entities
Enrich entities using information from Tenable.io. Supported entities: IP Address, Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight containing all of the retrieved information about the entity.|False|Boolean|true|



##### JSON Results
```json
[{"Entity":"EX201xxxxx","EntityResult":{"id":"11111111-aaaa-bbbb-cccc-dddddddddddd","has_agent":true,"has_plugin_results":true,"agent_uuid":"agent-uuid-1234-5678-90ab-cdef12345678","is_licensed":true,"types":["host","cloud"],"agent_names":["aws-prod-linux-01"],"operating_systems":["Amazon Linux 2","Linux Kernel 4.14.225-121.357.amzn2.x86_64"],"system_types":["general-purpose"],"manufacturer_tpm_ids":["TPM-8923-2234-5511"],"installed_software":["cpe:/a:apache:http_server:2.4.46","cpe:/a:openssl:openssl:1.1.1k","cpe:/a:tenable:nessus_agent:10.4.1"],"is_public":true,"network_device_serial_identifier":"NET-DEV-998877","custom_attributes":[{"id":"business_unit","value":"e-commerce"}],"sources":[{"name":"AWS","first_seen":"2023-01-15T08:00:00.000Z","last_seen":"2023-10-27T14:30:00.000Z"},{"name":"NESSUS_AGENT","first_seen":"2023-01-15T08:05:00.000Z","last_seen":"2023-10-27T15:00:00.000Z"}],"tags":[{"uuid":"tag-uuid-1111-2222","key":"Environment","value":"Production","added_by":"user-uuid-admin","added_at":"2023-02-01T12:00:00.000Z"}],"scan":{"first_scan_time":"2023-01-15T09:00:00.000Z","last_scan_time":"2023-10-27T15:00:00.000Z","last_authenticated_scan_date":"2023-10-26T23:00:00.000Z","last_licensed_scan_date":"2023-10-27T15:00:00.000Z","last_scan_id":"scan-uuid-5555-6666","last_schedule_id":"schedule-uuid-7777-8888","last_authentication_attempt_date":"2023-10-26T23:00:00.000Z","last_authentication_success_date":"2023-10-26T23:00:00.000Z","last_authentication_scan_status":"Success","last_scan_target":"10.0.1.50"},"cloud":{"aws":{"ec2_instance_ami_id":"ami-0abcdef1234567890","ec2_instance_id":"i-0123456789abcdef0","owner_id":"123456789012","availability_zone":"us-west-2a","region":"us-west-2","vpc_id":"vpc-01122334455667788","ec2_instance_group_name":"launch-wizard-1","ec2_instance_state_name":"running","ec2_instance_type":"t3.medium","subnet_id":"subnet-0aabbccddeeff0011","ec2_product_code":"ab12cd34","ec2_name":"prod-web-server-01"}},"third_party_ids":{"servicenow_sysid":"sysid-snow-12345","qualys_asset_ids":["12345678"],"qualys_host_ids":["98765432"]},"network":{"network_id":"00000000-0000-0000-0000-000000000000","network_name":"Default","bios_uuid":"42345678-1234-1234-1234-123456789012","ipv4s":["10.0.1.50","203.0.113.10"],"ipv6s":["2001:db8:85a3::8a2e:370:7334"],"fqdns":["prod-web-01.example.com","ec2-203-0-113-10.us-west-2.compute.amazonaws.com"],"mac_addresses":["00:11:22:33:44:55"],"hostnames":["ip-10-0-1-50"],"ssh_fingerprints":["SHA256:abcd1234abcd1234abcd1234abcd1234"],"network_interfaces":[{"name":"eth0","mac_addresses":["00:11:22:33:44:55"],"ipv4s":["10.0.1.50"],"ipv6s":["2001:db8:85a3::8a2e:370:7334"],"fqdns":["prod-web-01.example.com"],"virtual":false,"aliased":false}],"open_ports":[{"port":443,"protocol":"TCP","service_names":["https","www"],"first_seen":"2023-01-15T09:00:00.000Z","last_seen":"2023-10-27T15:00:00.000Z"}]},"timestamps":{"created_at":"2023-01-15T08:00:00.000Z","updated_at":"2023-10-27T15:05:00.000Z","first_seen":"2023-01-15T08:00:00.000Z","last_seen":"2023-10-27T15:00:00.000Z"},"tenable_agent_days_since_active":0,"ratings":{"acr":{"score":9.5},"aes":{"score":850}},"resource_tags":[{"key":"aws:cloudformation:stack-name","value":"ProdStack"},{"key":"CostCenter","value":"IT-Ops"}]}},{"Entity":"172.30.202.xxx","EntityResult":{"id":"22222222-eeee-ffff-aaaa-bbbbbbbbbbbb","has_agent":false,"has_plugin_results":true,"is_licensed":false,"terminated_by":"azure_admin_user@example.com","deleted_by":"tenable_manager@example.com","types":["host","cloud"],"operating_systems":["Microsoft Windows 10 Enterprise","Windows 10 Build 19044"],"system_types":["general-purpose"],"is_public":false,"sources":[{"name":"NESSUS_SCAN","first_seen":"2022-05-10T10:00:00.000Z","last_seen":"2022-12-01T09:00:00.000Z"}],"scan":{"first_scan_time":"2022-05-10T10:30:00.000Z","last_scan_time":"2022-12-01T09:00:00.000Z","last_authenticated_scan_date":"2022-12-01T09:00:00.000Z","last_licensed_scan_date":"2022-11-25T09:00:00.000Z","last_scan_id":"scan-uuid-1111-2222","last_authentication_attempt_date":"2022-12-01T09:00:00.000Z","last_authentication_success_date":"2022-12-01T09:00:00.000Z","last_authentication_scan_status":"Success - SMB"},"cloud":{"azure":{"vm_id":"azure-vm-uuid-1234-5678","resource_id":"/subscriptions/sub-id/resourceGroups/rg-name/providers/Microsoft.Compute/virtualMachines/win-workstation-01"}},"third_party_ids":{"mcafee_epo_guid":"{12345678-1234-1234-1234-123456789012}","mcafee_epo_agent_guid":"{87654321-4321-4321-4321-210987654321}","bigfix_asset_id":"9988776655","symantec_ep_hardware_keys":["A1B2C3D4E5"]},"network":{"network_id":"00000000-0000-0000-0000-000000000000","ipv4s":["192.168.1.105"],"fqdns":["win-workstation-01.corp.local"],"mac_addresses":["AA:BB:CC:DD:EE:FF"],"netbios_names":["WORKSTATION-01"],"hostnames":["win-workstation-01"],"network_interfaces":[{"name":"Ethernet0","mac_addresses":["AA:BB:CC:DD:EE:FF"],"ipv4s":["192.168.1.105"],"fqdns":["win-workstation-01.corp.local"]}]},"timestamps":{"created_at":"2022-05-10T10:00:00.000Z","updated_at":"2022-12-05T08:00:00.000Z","deleted_at":"2022-12-05T08:00:00.000Z","terminated_at":"2022-12-04T22:00:00.000Z","first_seen":"2022-05-10T10:00:00.000Z","last_seen":"2022-12-01T09:00:00.000Z"},"ratings":{"acr":{"score":4.0},"aes":{"score":200}},"resource_tags":[{"key":"Department","value":"Finance"}]}}]
```



#### Get Vulnerability Details
Retrieve vulnerability details from Tenable.io.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Plugin IDs|Specify a comma-separated list of plugin IDs for which you want to return details.|False|String||
|Create Insight|If enabled, action will create an insight containing information about all of the processed plugin ids.|False|Boolean|true|



##### JSON Results
```json
[{"plugin_id":11111,"info":{"count":1,"vuln_count":27,"recasted_count":0,"accepted_count":0,"description":"The remote service accepts connections encrypted using TLS 1.0. TLS 1.0 has a number of cryptographic design flaws. Modern implementations of TLS 1.0 mitigate these problems, but newer versions of TLS like 1.2 and 1.3 are designed against these flaws and should be used whenever possible.\n\nAs of March 31, 2020, Endpoints that aren’t enabled for TLS 1.2 and higher will no longer function properly with major web browsers and major vendors.\n\nPCI DSS v3.2 requires that TLS 1.0 be disabled entirely by June 30, 2018, except for POS POI terminals (and the SSL/TLS termination points to which they connect) that can be verified as not being susceptible to any known exploits.","synopsis":"The remote service encrypts traffic using an older version of TLS.","solution":"Enable support for TLS 1.2 and 1.3, and disable support for TLS 1.0.","discovery":{"seen_first":"2020-07-29T10:29:04.991Z","seen_last":"2021-07-06T10:11:11.706Z"},"severity":2,"plugin_details":{"family":"Service detection","modification_date":"2020-03-31T00:00:00Z","name":"TLS Version 1.0 Protocol Detection","publication_date":"2017-11-22T00:00:00Z","type":"remote","version":"1.9","severity":2},"reference_information":[],"risk_information":{"risk_factor":"Medium","cvss_vector":"AV:N/AC:H/Au:N/C:C/I:P/A:N","cvss_base_score":"6.1","cvss_temporal_vector":null,"cvss_temporal_score":null,"cvss3_vector":"AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:L/A:N","cvss3_base_score":"6.5","cvss3_temporal_vector":null,"cvss3_temporal_score":null,"stig_severity":null},"see_also":["https://tools.ietf.org/html/draft-ietf-tls-oldversions-deprecate-00"],"vulnerability_information":{"vulnerability_publication_date":null,"exploited_by_malware":null,"patch_publication_date":null,"exploit_available":null,"exploitability_ease":null,"asset_inventory":"True","default_account":null,"exploited_by_nessus":null,"in_the_news":null,"malware":null,"unsupported_by_vendor":null,"cpe":null,"exploit_frameworks":[]}}}]
```



#### Scan Endpoints
Initiate a scan on endpoints in Tenable.io. Supported entities: IP Address, Hostname. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan Name|Specify the name of the scan.|True|String||
|Policy Name|Specify the name of the policy that needs to be used for scanning.|True|String||
|Scanner Name|Specify the name of the scanner that should be used. If nothing is provided, action will use the default scanner from configuration.|False|String||
|Send Report To|Specify a comma-separated list of email addresses that need to receive the scan report.|False|String||



##### JSON Results
```json
{"info":{"owner":"hparker@siemplify.co","name":"Test","no_target":false,"folder_id":null,"control":true,"user_permissions":128,"schedule_uuid":"template-ae34e842-c9e1-7c39-4c43-xxxxxxxxxxxxxxxx","edit_allowed":false,"scanner_name":"scanner-name","policy":"Advanced Network Scan","shared":null,"object_id":126,"tag_targets":null,"acls":[{"permissions":0,"owner":null,"display_name":null,"name":null,"uuid":null,"id":null,"type":"default"},{"permissions":128,"owner":1,"display_name":"hparker@siemplify.co","name":"hparker@siemplify.co","uuid":"3385d69a-8829-4ee7-xxxxxxxxxx","id":2,"type":"user"}],"hostcount":1,"uuid":"a36cc900-b061-416d-a566-xxxxxxxxxxx","status":"completed","scan_type":"remote","targets":"172.30.xxx.xxx","alt_targets_used":false,"pci-can-upload":false,"scan_start":1627302001,"timestamp":1627302178,"is_archived":false,"reindexing":false,"scan_end":1627302178,"haskb":true,"hasaudittrail":true,"scanner_start":null,"scanner_end":null},"hosts":[{"asset_id":2,"host_id":2,"uuid":"c532eb31-74b7-43fa-8df3-xxxxxxxxx","hostname":"172.30.xxx.xxx","progress":"100-100/200-200","scanprogresscurrent":100,"scanprogresstotal":100,"numchecksconsidered":100,"totalchecksconsidered":100,"severitycount":{"item":[{"count":37,"severitylevel":0},{"count":9,"severitylevel":1},{"count":30,"severitylevel":2},{"count":17,"severitylevel":3},{"count":1,"severitylevel":4}]},"severity":94,"score":30127,"info":37,"low":9,"medium":30,"high":17,"critical":1,"host_index":0}],"vulnerabilities":[{"count":3,"plugin_id":25221,"plugin_name":"Remote listeners enumeration (Linux / AIX)","severity":0,"plugin_family":"Service detection","vuln_index":1},{"count":1,"plugin_id":10267,"plugin_name":"SSH Server Type and Version Information","severity":0,"plugin_family":"Service detection","vuln_index":2},{"count":1,"plugin_id":10881,"plugin_name":"SSH Protocol Versions Supported","severity":0,"plugin_family":"General","vuln_index":3},{"count":1,"plugin_id":11936,"plugin_name":"OS Identification","severity":0,"plugin_family":"General","vuln_index":4}],"comphosts":[],"compliance":[],"history":[{"history_id":14322559,"owner_id":2,"creation_date":1627302001,"last_modification_date":1627302178,"uuid":"a36cc900-b061-416d-xxxxxxxxxxxx","type":"remote","status":"completed","scheduler":0,"alt_targets_used":false,"is_archived":false}],"notes":[],"remediations":{"num_cves":195,"num_hosts":1,"num_remediated_cves":193,"num_impacted_hosts":1,"remediations":[{"vulns":10,"value":"5c6104606991eca499e23e6611e832cd","hosts":1,"remediation":"CentOS 7 : nss and nspr (CESA-2020:4076): Update the affected packages."},{"vulns":1,"value":"8b1df827f8efe13ca318f9b73de4edb6","hosts":1,"remediation":"CentOS 7 : polkit (CESA-2020:1135): Update the affected polkit packages."},{"vulns":3,"value":"b390f09333c7c9f20cf053af341e5114","hosts":1,"remediation":"CentOS 7 : curl (CESA-2020:5002): Update the affected curl, libcurl and / or libcurl-devel packages."}]}}
```



#### Ping
Test connectivity to the Tenable.io with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### List Scanners
List available scanners in Tenable.io.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Scanners To Return|Specify how many scanners to return. Default: 50. Max: 100.|False|String|50|



##### JSON Results
```json
[{"creation_date":1627296891,"distro":"es7-x86-64","engine_version":"18.15.0","group":false,"hostname":"scaner","id":200394,"ip_addresses":["172.30.xxx.xxx"],"key":"6201c49ba806af3cdc8611973b7831145c73ab3d31eb68xxxxxxxxxxxxxxx","last_connect":1627302041,"last_modification_date":1627298226,"linked":1,"loaded_plugin_set":"202107260512","name":"scanner-name","network_name":"Default","num_hosts":0,"num_scans":1,"num_sessions":0,"num_tcp_sessions":0,"owner":"system","owner_id":1,"owner_name":"system","owner_uuid":"3a15b6cd-9412-4274-xxxxxxxxxxxx","platform":"LINUX","pool":false,"scan_count":1,"shared":1,"source":"service","status":"on","timestamp":1627298226,"type":"managed","ui_build":"271","ui_version":"8.15.0","user_permissions":128,"uuid":"3b984f25-6e4b-4d1f-8ad7-xxxxxxxxxxx","remote_uuid":"c5a26121-c728-5986-1077-xxxxxxxxxxxxxx","supports_remote_logs":true,"supports_webapp":false},{"creation_date":1574892411,"group":true,"id":120044,"key":"1e53e08b84c583fd54211e85b2bfcf575f7b803c7eae4xxxxxxxxxxxxxxxxx","last_connect":null,"last_modification_date":1627296829,"license":{"record_id":"0016000001Ey1UDAAZ","type":"vm","activation_code":"6FSL-xxxxxxxxx","agents":-1,"ips":100,"scanners":-1,"users":-1,"enterprise_pause":false,"expiration_date":1654819199,"evaluation":false,"apps":{"pci":{"mode":"basic"}},"scanners_used":1,"agents_used":0},"linked":1,"name":"EU Frankfurt Cloud Scanners","network_name":"Default","num_scans":0,"owner":"system","owner_id":1,"owner_name":"system","owner_uuid":"3a15b6cd-9412-4274-xxxxxxxxxxxx","pool":true,"scan_count":0,"shared":1,"source":"service","status":"on","timestamp":1627296829,"type":"local","user_permissions":64,"uuid":"00000000-0000-0000-0000-0000","supports_remote_logs":false,"supports_webapp":true}]
```



#### List Policies
List available policies in Tenable.io.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Policies To Return|Specify how many policies to return. Default: 50. Max: 100.|False|String|50|



##### JSON Results
```json
[{"no_target":"false","template_uuid":"731a8e52-3ea6-a291-ec0a-d2ff0619cxxxxxxxxxxxxxxxxxx","description":null,"name":"Koko","owner":"hparker@siemplify.co","visibility":"private","shared":0,"user_permissions":128,"last_modification_date":1625744218,"creation_date":1625744218,"owner_id":2,"id":73},{"no_target":"false","template_uuid":"731a8e52-3ea6-a291-ec0a-d2ff0619cxxxxxxxxxxxxxxxxx","description":null,"name":"Koko_01","owner":"hparker@siemplify.co","visibility":"private","shared":0,"user_permissions":128,"last_modification_date":1625744230,"creation_date":1625744230,"owner_id":2,"id":74}]
```









## Connectors
#### TenableIO - Vulnerabilities Connector
Pull vulnerabilities from Tenable.io. Note: connector works with plugin families in whitelist.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|event_type|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|300|
|API Root|API Root of the Tenable.io instance.|True|String|https://cloud.tenable.com|
|Access Key|Access Key of the Tenable.io instance.|True|Password|*****|
|Secret Key|Secret Key of the Tenable.io instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Tenable.io server is valid.|False|Boolean|true|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch vulnerabilities. If nothing is provided, the connector will fetch all vulnerabilities. Possible values: Info, Low, Medium, High, Critical|False|Integer|Medium|
|Status Filter|Status filter for the connector. It works with comma-separated values. If nothing is provided, the connector will ingest vulnerabilities with "open", "reopened" statuses. Possible values: open, reopened, fixed.|False|String|open, reopened|
|Max Days Backwards|Number of days before the first connector iteration to retrieve vulnerabilities from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Default: 30 days. Note: this parameter will return vulnerabilities that were opened/reopened/fixed in the timeframe that is specified in "Max Days Backwards".|False|Integer|30|
|Grouping Mechanism|Grouping mechanism that will be used to create Siemplify Alerts. Possible values: Host, Vulnerability, None. If Host is provided, the connector will create 1 Siemplify alert containing all of the vulnerabilities per chunk related to the host. If Vulnerability is provided, the connector will create 1 Siemplify Alert containing information about all of the hosts that have that vulnerability in the scope of 1 chunk. If None or invalid value is provided, the connector will create a new Siemplify alert for each separate vulnerability per host.|True|String|Host|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




