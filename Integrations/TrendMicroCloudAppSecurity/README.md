
# TrendMicroCloudAppSecurity

Trend Micro Cloud App Security enables you to embrace the efficiency of cloud services while maintaining security. It protects incoming and internal Office 365 email from advanced malware and other threats, and enforces compliance on other cloud file-sharing services, including Box, Dropbox, Google Drive, SharePoint® Online, and OneDrive® for Business. Cloud App Security integrates directly with Office 365 and other services using APIs, maintaining all user functionality without rerouting email traffic or setting up a web proxy.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://api-eu.tmcas.trendmicro.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|validators-0.33.0-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich entities with information from Trend Micro Cloud App Security. Supported entities: URL, Hash and Email (User entity that matches email address pattern). Note: action will use the domain part out of the URL during the enrichment.
Timeout - 600 Seconds



##### JSON Results
```json
{"blocked_urls": ["https://url.com"], "blocked_senders": ["test1@test.com", "test2@test.com"], "blocked_hashes": ["85136c79cbf9fe36bb9d05d0639c70c265c18xxx"]}
```



#### Add Entities To Blocklist
Add entities to a blocklist in Trend Micro Cloud App Security. Supported entities: URL, Hash and Email (User entity that matches email address pattern). Note: only SHA-1 hashes are supported.
Timeout - 600 Seconds



#### Ping
Test connectivity to the Trend Micro CloudApp Security with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Mitigate Accounts
Perform mitigation actions on the user account via Trend Micro Cloud App Security. Note: only Exchange accounts are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mitigation Action|Specify what mitigation action should be applied.|True|List|Disable Account|
|Email Addresses|Specify a comma-separated list of email addresses that need to be mitigated.|True|String||



#### Entity Email Search
Search emails based on entities in Trend Micro Cloud App Security. Supported entities: URL, Hash, Email (User entity that matches email address pattern), Email Subject, File Name, IP. Note: only SHA-1 and SHA256 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Days Backwards|Specify how many days backwards to look for emails. Maximum is 90. Default: 30.|False|String|30|
|Max Emails To Return|Specify how many emails to return. Default: 100.|False|String|100|



##### JSON Results
```json
[{"mail_message_sender": "azure-noreply@microsoft.com", "mail_message_recipient": ["user@test.com"], "mail_message_subject": "Azure Security Center has detected suspicious activity in your environment", "mailbox": "user@test.com", "mail_urls": ["https://azure.microsoft.com/emailtrackingpixel/?p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8%3D", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Fwww.youtube.com%2Fuser%2Fwindowsazure&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1mb290ZXIlM0F5b3V0dWJl", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Fwww.linkedin.com%2Fshowcase%2Fmicrosoft-developers&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1mb290ZXIlM0FsaW5rZWRpbg%3D%3D", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Fwww.facebook.com%2Fmicrosoftazure&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1mb290ZXIlM0FmYWNlYm9vaw%3D%3D", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Ftwitter.com%2Fazure&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1mb290ZXIlM0F0d2l0dGVy", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Fportal.azure.com%2F%23blade%2FMicrosoft_Azure_Security%2FSecurityContactBlade%2FsubscriptionId%2Fa052d33b-b7c4-4dc7-9e17-5c89ea594669&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1wb3J0YWwlM0FzZWN1cml0eS1jb250YWN0", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Fportal.azure.com%2F%23blade%2FMicrosoft_Azure_Security%2FAlertBlade%2FalertId%2F2517889194552039666_04942809-0b90-4e3a-b7d2-6369012a0328%2FsubscriptionId%2Fa052d33b-b7c4-4dc7-9e17-5c89ea594669%2FreferencedFrom%2Femail%2Flocation%2Fwesteurope&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1zZWN1cml0eS1hbGVydC1ibGFkZQ%3D%3D", "https://azure.microsoft.com/email/?destination=https%3A%2F%2Fgo.microsoft.com%2Ffwlink%2F%3FLinkId%3D521839&p=bT0yZmU4YjM1OC05YTlmLTRmNTctOGFjMi03MWNlZDI3NGI3NmYmcz1hMDUyZDMzYi1iN2M0LTRkYzctOWUxNy01Yzg5ZWE1OTQ2NjkmdT1hZW8mbD1wcml2YWN5LXN0YXRlbWVudA%3D%3D", "https://aeocdn.azureedge.net/mediahandler/azure-emails-templates/production/shared/images/templates/shared/images/icons/service-security-center.png?v=2020-02-11", "https://aeocdn.azureedge.net/mediahandler/azure-emails-templates/production/branch-master/build-229380/images/templates/securitycenter/alertextended/resource.png", "https://aeocdn.azureedge.net/mediahandler/azure-emails-templates/production/branch-master/build-229380/images/templates/securitycenter/alertextended/microsoft.png"], "source_domain": "microsoft.com", "source_ip": "65.55.52.234", "mail_message_delivery_time": "2021-02-15T09:30:41.000Z", "mail_message_id": "<2fe8b358-9a9f-4f57-8ac2-71ced274bxxx@az.westeurope.production.microsoft.com>", "mail_unique_id": "AAkALgAAAAAAHYQDEapmEc2byACqAC-EWg0AjfEciVgIUEq0vwagO2PKqQAAwF2fkxxx", "mail_attachments": [], "mail_internet_headers": [{"Value": "azure-noreply@microsoft.com", "HeaderName": "Return-Path"}, {"Value": "spf=pass (sender IP is 0.0.0.1) smtp.mailfrom=microsoft.com; test.com; dkim=pass (signature was verified) header.d=microsoft.com;test.com; dmarc=pass action=none header.from=microsoft.com;compauth=pass reason=100", "HeaderName": "Authentication-Results"}]}]
```



#### Mitigate Emails
Delete or quarantine emails using Trend Micro Cloud App Security. Note: for Gmail you can only delete emails. Note: Currently action only initiates a mitigation, but doesn't check the status of mitigation execution.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mitigation Action|Specify what mitigation action should be applied.|True|List|Delete|
|Service|Specify the service the is used for emails.|True|List|Gmail|
|Message IDs|Specify a comma-separated list of message ids that need to be mitigated.|True|String||









