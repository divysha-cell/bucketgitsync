# DRP Violations Connector
DRP Violations Connector


Integration: Group-IB-DRP

Integration Version: 1

Device Product Field: title

Event Name Field: id
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|API login| your DRP email  |True|example@email.me|
|API key|your DRP API token |True|*****|
|API URL|DRP URL|True|https://drp.group-ib.com/client_api/|
|Verify SSL|Verify the server's SSL certificate.|False|true|
| Case name  |Violation URL |True|Violation URL |
|Case severity|Severity|True|Medium|
|Case type  |Type|True|Violations|
|Start date |leave blank (defaults to 1 day back) |False||
|Brand IDs|Filtering by company brands|False||
|Approve States|1 - Not required; 2 - Rejected; 3 - Under review; 4 - approved|False||
|Subtypes|1 - counterfeit; 2 - piracy; 3 - partner_policy_compliance; 4 - trademark; 5 - malware; 6 - phishing; 7 - fraud; 8 - no_violation|False||
|Section|1 - Web; 2 - Mobile apps; 3 - Marketplace; 4 - Social networks; 5 - Advertising; 6 - Instant messengers|False||


Addon !@12