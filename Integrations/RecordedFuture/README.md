
# RecordedFuture

Recorded Future's unique technology collects and analyzes vast amounts of data to deliver relevant cyber threat insights in real-time

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Url||True|String|https://api.recordedfuture.com|
|Api Key||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|


## Actions
#### Enrich CVE
Query the RecordedFuture to get more information about the CVE.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a CVE to be marked malicious. Has a range of 0-99. Has the following levels:  Very Critical: 90-99  Critical: 80-89  High: 65-79  Medium: 25-64  Low: 5-24  None: 0|True|String|25|
|Include Related Entities|If enabled, action will get information about related entities.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "CVE-1999-xxx", "EntityResult": {"relatedEntities": [{"type": "RelatedCyberVulnerability", "entities": [{"count": 8, "entity": {"id": "LExxx6r", "name": "CVE-2006-xxxx", "type": "CyberVulnerability", "description": "The E4X implementation in Mozilla Firefox before 1.5.0.1, Thunderbird 1.5 if running Javascript in mail, and SeaMonkey before 1.0 exposes the internal \"AnyName\" object to external interfaces, which allows multiple cooperating domains to exchange information in violation of the same origin restrictions."}}, {"count": 8, "entity": {"id": "LExxxxzP", "name": "CVE-1999-xxxx", "type": "CyberVulnerability", "description": "Buffer overflow in Solaris sadmind allows remote attackers to gain root privileges using a NETMGT_PROC_SERVICE request."}}, {"count": 8, "entity": {"id": "LxxxAh8", "name": "MS06-xxx", "type": "CyberVulnerability"}}, {"count": 6, "entity": {"id": "LzzxxAdu", "name": "CWE-xxx", "type": "CyberVulnerability"}}, {"count": 6, "entity": {"id": "LxxdV-", "name": "CVE-2014-xxxx", "type": "CyberVulnerability", "description": "Multiple cross-site request forgery (CSRF) vulnerabilities in PHPJabbers Appointment Scheduler 2.0 allow remote attackers to hijack the authentication of administrators for requests that (1) conduct cross-site scripting (XSS) attacks via the i18n[1][name] parameter in a pjActionCreate action to the pjAdminServices controller or (2) add an administrator via a pjActionCreate action to the pjAdminUsers controller."}}, {"count": 6, "entity": {"id": "M0jXxx", "name": "CVE-2014-xxxxx", "type": "CyberVulnerability", "description": "Cross-site request forgery (CSRF) vulnerability in the SEO Plugin LiveOptim plugin before 1.1.4-free for WordPress allows remote attackers to hijack the authentication of administrators for requests that change plugin settings via unspecified vectors.  NOTE: some of these details are obtained from third party information."}}, {"count": 2, "entity": {"id": "NWxxEF", "name": "CVE-1999-xxxx", "type": "CyberVulnerability", "description": "The Webcom CGI Guestbook programs wguest.exe and rguest.exe allow a remote attacker to read arbitrary files using the \"template\" parameter."}}, {"count": 2, "entity": {"id": "NWlSxx", "name": "CVE-1999-xxxx", "type": "CyberVulnerability", "description": "CGI PHP mlog script allows an attacker to read any file on the target server."}}, {"count": 2, "entity": {"id": "xxUtM", "name": "CVE-2000-xxxx", "type": "CyberVulnerability", "description": "SGI InfoSearch CGI program infosrch.cgi allows remote attackers to execute commands via shell metacharacters."}}, {"count": 1, "entity": {"id": "KxxKD", "name": "CVE-2014-xxxx", "type": "CyberVulnerability"}}, {"count": 1, "entity": {"id": "KeKxxx", "name": "CWE-xxx", "type": "CyberVulnerability"}}, {"count": 1, "entity": {"id": "Kxxxpf", "name": "CWE-xxx", "type": "CyberVulnerability"}}, {"count": 1, "entity": {"id": "LBxxTK", "name": "CWE-xx", "type": "CyberVulnerability"}}, {"count": 1, "entity": {"id": "LxxHYa", "name": "CWE-28", "type": "CyberVulnerability"}}, {"count": 1, "entity": {"id": "LExxxA", "name": "CVE-2009-xxxx", "type": "CyberVulnerability", "description": "Heap-based buffer overflow in Xpdf 3.02pl2 and earlier, CUPS 1.3.9, and probably other products, allows remote attackers to execute arbitrary code via a PDF file with crafted JBIG2 symbol dictionary segments."}}, {"count": 1, "entity": {"id": "LFxxmr", "name": "CVE-2002-xxxx", "type": "CyberVulnerability", "description": "Vulnerabilities in a large number of SNMP implementations allow remote attackers to cause a denial of service or gain privileges via SNMPv1 trap handling, as demonstrated by the PROTOS c06-SNMPv1 test suite.  NOTE: It is highly likely that this candidate will be SPLIT into multiple candidates, one or more for each vendor.  This and other SNMP-related candidates will be updated when more accurate information is available."}}, {"count": 1, "entity": {"id": "MIxxuT", "name": "CWE-24", "type": "CyberVulnerability"}}, {"count": 1, "entity": {"id": "NWlTxx", "name": "CVE-1999-xxxx", "type": "CyberVulnerability", "description": "Remote attackers can perform a denial of service in WinGate machines using a buffer overflow in the Winsock Redirector Service."}}, {"count": 1, "entity": {"id": "NxxNq", "name": "CVE-2000-xxxx", "type": "CyberVulnerability", "description": "Red Hat userhelper program in the usermode package allows local users to gain root access via PAM and a .. (dot dot) attack."}}, {"count": 1, "entity": {"id": "Vbmxxq", "name": "CVE-2018-xxxx", "type": "CyberVulnerability", "description": "The Password Manager Extension in Abine Blur 7.8.242* before 7.8.2428 allows attackers to bypass the Multi-Factor Authentication and macOS disk-encryption protection mechanisms, and consequently exfiltrate secured data, because the right-click context menu is not secured."}}, {"count": 1, "entity": {"id": "Xyxxbc", "name": "CVE-2018-xxxx", "type": "CyberVulnerability", "description": "Vulnerability in the MySQL Server component of Oracle MySQL (subcomponent: Server: Parser). Supported versions that are affected are 5.5.61 and prior, 5.6.41 and prior, 5.7.23 and prior and 8.0.12 and prior. Easily exploitable vulnerability allows low privileged attacker with network access via multiple protocols to compromise MySQL Server. Successful attacks of this vulnerability can result in unauthorized ability to cause a hang or frequently repeatable crash (complete DOS) of MySQL Server. CVSS 3.0 Base Score 6.5 (Availability impacts). CVSS Vector: (CVSS:3.0/A:N/AX:L/PX:L/UX:N/S:UX/C:N/I:N/A:H)."}}]}, {"type": "RelatedHash", "entities": [{"count": 2, "entity": {"id": "hash:20002471162cb920b9b22e7d14f3b72b0dd6d922c747da2dexxxx40c3", "name": "20002471162cb920b9b22e7d14f3b72b0dd6d922c747da2dxxxx04840c3", "type": "Hash"}}, {"count": 2, "entity": {"id": "hash:23c777f04e17ba902fb212be443fxxxxf9fe4ecb55aeacaec", "name": "23c777f04e17ba902fb212be443ffxxxxx853689a009f9fe4ecb55aeacaec", "type": "Hash"}}, {"count": 2, "entity": {"id": "hash:4a4dd69670e337a50e88521e3eb886052179dbe00372cxxxxx7e5f58be3", "name": "4a4dd69670e337a50e88521e3eb886052179dbe00372cxxxx257e5f58be3", "type": "Hash"}}, {"count": 2, "entity": {"id": "hash:5d202c5d2fc1dfa21de65e9a0f0ba4fd8203xxxxxxxxxx473ddc85a1a290f077cc", "name": "5d202c5d2fc1dfa21de65e9a0f0ba4fd8203c7edfxxxxxxx5a1a290f077cc", "type": "Hash"}}, {"count": 1, "entity": {"id": "hash:84e8c91af448fc5c7ad3b060dc90a9cd310xxxxxxxxx242031647b31aa0841360", "name": "84e8c91af448fc5c7ad3b060dc90a9cd310e8c7005xxxxxx647b31aa0841360", "type": "Hash"}}]}, {"type": "RelatedTechnology", "entities": [{"count": 14, "entity": {"id": "B_XxB", "name": "CGI", "type": "Technology"}}, {"count": 14, "entity": {"id": "I5XxxdQ", "name": "Computer Science", "type": "Technology"}}, {"count": 9, "entity": {"id": "B56xXu", "name": "SHA-256", "type": "Technology"}}, {"count": 5, "entity": {"id": "OxxXdE", "name": "arachnids", "type": "Technology"}}, {"count": 1, "entity": {"id": "CXxcF", "name": "Computer Software", "type": "Technology"}}, {"count": 1, "entity": {"id": "BM8XxQ", "name": "Computer Programming", "type": "Technology"}}, {"count": 1, "entity": {"id": "I50CXx", "name": "Computer Networking", "type": "Technology"}}, {"count": 1, "entity": {"id": "I50CXX", "name": "Computing Platform", "type": "Technology"}}]}, {"type": "RelatedInternetDomainName", "entities": [{"count": 8, "entity": {"id": "idn:binxx.com", "name": "binxx.com", "type": "InternetDomainName"}}, {"count": 8, "entity": {"id": "idn:ntbugxxx.com", "name": "ntbugxxx.com", "type": "InternetDomainName"}}, {"count": 2, "entity": {"id": "idn:moxxx.com", "name": "moxxx.com", "type": "InternetDomainName"}}]}, {"type": "RelatedAttackVector", "entities": [{"count": 28, "entity": {"id": "JPv_Xx", "name": "Privilege Escalation", "type": "AttackVector"}}, {"count": 28, "entity": {"id": "PGG2Xx", "name": "Abuse of Application Functionality", "type": "AttackVector"}}, {"count": 25, "entity": {"id": "JNCaXx", "name": "Remote Command Execution", "type": "AttackVector"}}, {"count": 14, "entity": {"id": "27rxX", "name": "Command Injection", "type": "AttackVector"}}, {"count": 1, "entity": {"id": "JUJXx_", "name": "Remote Code Execution", "type": "AttackVector"}}, {"count": 1, "entity": {"id": "PGG2xXx", "name": "Target Destination Manipulation", "type": "AttackVector"}}]}, {"type": "RelatedProduct", "entities": [{"count": 20, "entity": {"id": "TS4xxX", "name": "MITRE ATT&CK Framework ", "type": "Product"}}, {"count": 1, "entity": {"id": "CDx-X_", "name": "Perl", "type": "Product"}}]}], "timestamps": {"firstSeen": "1996-03-20T05:00:00.000Z", "lastSeen": "2020-11-05T13:01:54.912Z"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/NWlSMxxxxx", "risk": {"criticalityLabel": "High", "score": 65, "evidenceDetails": [{"mitigationString": "", "timestamp": "2020-11-18T13:33:15.563Z", "criticalityLabel": "High", "evidenceString": "1 sighting on 1 source: Recorded Future Vulnerability Analysis. CVSS v2 Score (7.7) calculated using NIST reported CVSS Base Score (10) and Recorded Future Temporal Metrics. Base vector string: AV:N/AC:L/Au:N/Cxx:C/IX:C/AX:C. Temporal vector string: E:U/RLx:XxX/RC:U.", "rule": "NIST Severity: High", "criticality": 3}], "riskString": "1/21", "rules": 1, "criticality": 3, "riskSummary": "1 of 21 Risk Rules currently observed."}}}, {"Entity": "CVE-2014-xxxx", "EntityResult": {"relatedEntities": [{"type": "RelatedCyberVulnerability", "entities": [{"count": 16, "entity": {"id": "Kgx3xx", "name": "CVE-2014-xxxx", "type": "CyberVulnerability", "description": "Buffer overflow in client/mysql.cc in Oracle MySQL and MariaDB before 5.5.35 allows remote database servers to cause a denial of service (crash) and possibly execute arbitrary code via a long server version string."}}, {"count": 16, "entity": {"id": "LBbxX", "name": "CWE-xx", "type": "CyberVulnerability"}}, {"count": 13, "entity": {"id": "Lm_xx-", "name": "CVE-2014-xxxx", "type": "CyberVulnerability", "description": "** REJECT **  DO NOT USE THIS CANDIDATE NUMBER. ConsultIDs: None.  Reason: This ID is frequently used as an example of the 2014 CVE-ID syntax change, which allows more than 4 digits in the sequence number. Notes: See references."}}, {"count": 11, "entity": {"id": "SuAxx_", "name": "CVE-2013-xxxx", "type": "CyberVulnerability"}}, {"count": 8, "entity": {"id": "QQxX_j", "name": "CVE-2014-xxxx", "type": "CyberVulnerability"}}, {"count": 6, "entity": {"id": "NWlKxx", "name": "CVE-1999-xxxx", "type": "CyberVulnerability", "description": "Execute commands as root via buffer overflow in Tooltalk database server (rpc.ttdbserverd)."}}, {"count": 1, "entity": {"id": "NWlSxxx", "name": "CVE-1999-xxxx", "type": "CyberVulnerability", "description": "phf CGI program allows remote command execution through shell metacharacters."}}]}], "timestamps": {"firstSeen": "2013-11-07T20:33:07.487Z", "lastSeen": "2020-06-02T15:53:26.740Z"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/KVxxYIxxx", "risk": {"criticalityLabel": "None", "score": 0, "evidenceDetails": [], "riskString": "0/21", "rules": 0, "criticality": 0, "riskSummary": "No Risk Rules are currently observed."}}}]
```



#### Add Analyst Note
Add an analyst note to previously enriched entities in Siemplify, to Recorded Future entities. Action will add the note to the relevant scope entities. Note: If entity will not contain the Recorded Future ID field - this action will perform “Enrich IOC” action on it for better results. You can choose whether to update the entity with the enrichment data or not.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Note Title|Specify the title for the note|True|String|Note Title|
|Note Text|Specify the Text for the note|True|String|Note Text|
|Note Source|Specify the RF ID for note source; the API explorer shows what the RF IDs are accessible to the user whose API token is enabled. For example,  VWKdVr is the RF ID for an analyst note and is only available to user in the same enterprise account in Recorded Future.|True|String||
|Topic|Specify the relevant Note topic from the list, if needed.|False|List|None|
|Enrich Entity?|Specify whether the action should enrich the entity with the “Enrich IOC” output.|False|Boolean|true|



#### Get CVE Related Entities
Query the RecordedFuture to get related entities for the CVE.
Timeout - 600 Seconds



#### Enrich Hash
Query the RecordedFuture to get more information about the hash.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a Hash to be marked malicious. Has a range of 0-89. Has the bands levels:  No Suspicious/Malicious content: 0  Unusual: 5-24  Suspicious: 25-64  Malicious: 65-89|True|String|25|
|Include Related Entities|If enabled, action will get information about related entities.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "8743b52063cd84097a65d1633f5xxxx", "EntityResult": {"hashAlgorithm": "MD5", "timestamps": {"firstSeen": "2014-05-19T05:34:43.272Z", "lastSeen": "2020-09-12T04:32:40.322Z"}, "risk": {"criticalityLabel": "Suspicious", "score": 30, "evidenceDetails": [{"mitigationString": "", "timestamp": "2015-09-16T00:00:00.000Z", "criticalityLabel": "Suspicious", "evidenceString": "2 sightings on 1 source: National Common Vulnerabilities and Exposures (CVE) Database. 2 related malwares: Remote Access Trojan, Poison Ivy (Darkmoon). Most recent link (Sep 16, 2015): https://csrc.nist.gov/CSRC/media/Presentations/Automated-Indicator-Sharing/images-media/day2_info-sharing.pdf", "rule": "Linked to Malware", "criticality": 2}, {"mitigationString": "", "timestamp": "2020-02-14T06:25:58.631Z", "criticalityLabel": "Suspicious", "evidenceString": "1 sighting on 1 source: DOCPlayer. 1 related attack vector: Password Cracking. Most recent link (Feb 14, 2020): http://docplayer.net/xxx-xx-xxxx-Password-cracking-demystified-xxx-williams-alaska-usa-federal-credit-union.html", "rule": "Linked to Attack Vector", "criticality": 2}], "riskString": "2/13", "rules": 2, "criticality": 2, "riskSummary": "2 of 13 Risk Rules currently observed."}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/hash%3A8743b52063cd84097a65d1633f5xxxxx", "relatedEntities": [{"type": "RelatedMalwareCategory", "entities": [{"count": 2, "entity": {"id": "E0yxxx", "name": "Remote Access Trojan", "type": "MalwareCategory"}}]}, {"type": "RelatedHash", "entities": [{"count": 3, "entity": {"id": "hash:01dfae6e5d4d90d989262232595xxxxx", "name": "01dfae6e5d4d90d989262232595xxxxx", "type": "Hash"}}, {"count": 2, "entity": {"id": "hash:b4b9b02e6f09a9bd760f388b673xxxx", "name": "b4b9b02e6f09a9bd760f388b673xxxx", "type": "Hash"}}, {"count": 2, "entity": {"id": "hash:b89eaac7e61417341b710b727768294d0exxxxx", "name": "b89eaac7e61417341b710b727768294d0exxxxx", "type": "Hash"}}, {"count": 2, "entity": {"id": "hash:cac35ec206d868b7d7cb0b55f31d9425bxxxx", "name": "cac35ec206d868b7d7cb0b55f31d9425b0xxxx", "type": "Hash"}}]}, {"type": "RelatedInternetDomainName", "entities": [{"count": 1, "entity": {"id": "idn:hash.xxx", "name": "hash.xxx", "type": "InternetDomainName"}}]}, {"type": "RelatedMalware", "entities": [{"count": 2, "entity": {"id": "JQZJxxx", "name": "Poison Ivy (Darkmoon)", "type": "Malware"}}]}, {"type": "RelatedAttackVector", "entities": [{"count": 1, "entity": {"id": "JuB4xX", "name": "Password Cracking", "type": "AttackVector"}}]}, {"type": "RelatedProduct", "entities": [{"count": 3, "entity": {"id": "EzNSxXx", "name": "Cisco IOS", "type": "Product"}}]}]}}, {"Entity": "e0d123e5f316bef78bfdf5a00883xxxx", "EntityResult": {"hashAlgorithm": "MD5", "timestamps": {"firstSeen": "2016-09-19T00:48:55.609Z", "lastSeen": "2019-01-22T23:00:48.923Z"}, "risk": {"criticalityLabel": "None", "score": 0, "evidenceDetails": [], "riskString": "0/12", "rules": 0, "criticality": 0, "riskSummary": "No Risk Rules are currently observed."}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/hash%3Ae0d123e5f316bef78bfdf5a00883xxxx", "relatedEntities": []}}]
```



#### Enrich IOC
Fetch information about multiple entities, with different types, from Siemplify. Note - we recommend using this action first, and then, if additional information is needed - use the other enrich methods.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for each entity to be marked is suspicious.|True|String|25|



##### JSON Results
```json
[{"Entity": "CVE-1999-xxxx", "EntityResult": {"entity": {"id": "xNxWXlMx", "name": "CVE-1999-xxx", "type": "CyberVulnerability", "description": "phf CGI program allows remote command execution through shell metacharacters."}, "risk": {"level": 3.0, "rule": {"count": 1, "mostCritical": "NIST Severity: High", "maxCount": 21, "evidence": {"nistHigh": {"count": 1.0, "timestamp": "2020-09-30T23:01:08.493Z", "description": "1 sighting on 1 source: Recorded Future Vulnerability Analysis. CVSS v2 Score (7.7) calculated using NIST reported CVSS Base Score (10) and Recorded Future Temporal Metrics. Base vector string: AV:N/AC:LX/AX:NX/Cx:C/I:C/A:C. Temporal vector string: E:Ux/RxX:X/RCx:U.", "rule": "NIST Severity: High", "mitigation": "", "level": 3.0}}, "summary": [{"count": 1.0, "level": 3.0}]}, "context": {"malware": {"rule": {"count": 0, "maxCount": 2}, "score": 0.0}, "public": {"rule": {"maxCount": 22}, "summary": [{"count": 1.0, "level": 3.0}], "mostCriticalRule": "NIST Severity: High", "score": 65.0}}, "score": 65.0}}}, {"Entity": "CVE-2014-xxxx", "EntityResult": {"entity": {"id": "KXXIxKDx", "name": "CVE-2014-xxxx", "type": "CyberVulnerability"}, "risk": {"level": 0.0, "rule": {"count": 0, "mostCritical": "", "summary": [], "maxCount": 21}, "context": {"malware": {"rule": {"count": 0, "maxCount": 2}, "score": 0.0}, "public": {"rule": {"maxCount": 22}, "summary": [], "mostCriticalRule": "", "score": 0.0}}, "score": 0.0}}}]
```



#### Enrich IP
Query the RecordedFuture to get more information about the IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for an IP to be marked malicious. Has a range of 0-99. Below is the band levels:  Very Malicious: 90-99  Malicious: 65-89  Suspicious: 25-64  Unusual: 5-24  No Malicious content: 0|True|String|25|
|Include Related Entities|If enabled, action will get information about related entities.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "127.x.x.x", "EntityResult": {"location": {"asn": null, "location": {"continent": null, "city": null, "country": null}, "cidr": {"id": "ip:127.x.x.x/8", "name": "ip:127.x.x.x/8", "type": "IpAddress"}, "organization": null}, "timestamps": {"firstSeen": "2011-07-18T22:04:42.000Z", "lastSeen": "2020-11-18T17:16:34.634Z"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/ip%3Aip:127.x.x.x", "relatedEntities": [{"type": "RelatedMalwareCategory", "entities": [{"count": 120064, "entity": {"id": "0eXixxx", "name": "Computer Worm", "type": "MalwareCategory"}}, {"count": 9357, "entity": {"id": "0e4xxX", "name": "Computer virus", "type": "MalwareCategory"}}]}], "risk": {"criticalityLabel": "None", "score": 0, "evidenceDetails": [], "riskString": "0/53", "rules": 0, "criticality": 0, "riskSummary": "No Risk Rules are currently observed."}}}, {"Entity": "192.x.x.x", "EntityResult": {"location": {"asn": null, "location": {"continent": null, "city": null, "country": null}, "cidr": {"id": "ip:192.xx.x.x/2x", "name": "192.xx.x.x/2x", "type": "IpAddress"}, "organization": null}, "timestamps": {"firstSeen": "2012-01-22T19:57:51.443Z", "lastSeen": "2020-11-18T15:25:33.173Z"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/ip%3A192.xx.x.x", "relatedEntities": [{"type": "RelatedMalwareCategory", "entities": [{"count": 27, "entity": {"id": "0e4xxx", "name": "Computer virus", "type": "MalwareCategory"}}, {"count": 15, "entity": {"id": "0efxxxx", "name": "Trojan", "type": "MalwareCategory"}}]}], "risk": {"criticalityLabel": "None", "score": 0, "evidenceDetails": [], "riskString": "0/53", "rules": 0, "criticality": 0, "riskSummary": "No Risk Rules are currently observed."}}}]
```



#### Enrich Host
Query the RecordedFuture to get more information about the Host.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a Host to be marked malicious. Has a range of 0-99. Below is the band levels:  Very Malicious: 90-99  Malicious: 65-89  Suspicious: 25-64  Unusual: 5-24  No Malicious content: 0|True|String|25|
|Include Related Entities|If enabled, action will get information about related entities.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "xxxname.com", "EntityResult": {"relatedEntities": [{"type": "RelatedMalwareCategory", "entities": [{"count": 5362, "entity": {"id": "0efxxx", "name": "Trojan", "type": "MalwareCategory"}}, {"count": 2379, "entity": {"id": "0fL5xxx", "name": "Adware", "type": "MalwareCategory"}}, {"count": 1307, "entity": {"id": "J0Nl-xxx", "name": "Ransomware", "type": "MalwareCategory"}}, {"count": 1159, "entity": {"id": "0edxxx", "name": "Botnet", "type": "MalwareCategory"}}]}], "timestamps": {"firstSeen": "2009-01-23T02:00:08.000Z", "lastSeen": "2020-11-18T17:59:31.857Z"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/idn%xxxname.com", "risk": {"criticalityLabel": "Unusual", "score": 24, "evidenceDetails": [{"mitigationString": "", "timestamp": "2018-02-14T14:12:27.000Z", "criticalityLabel": "Unusual", "evidenceString": "1 sighting on 1 source: DHS Automated Indicator Sharing. 1 report: Domain Masquerading Websites Identified, from NCCIC, Government Facilities Sector, NCCIC:STIX_Package-xxb2aa2b-xx-4576-xxx-454c4xx200 (Feb 14, 2018).", "rule": "Historically Reported by DHS AIS", "criticality": 1}, {"mitigationString": "", "timestamp": "2019-12-26T22:54:53.000Z", "criticalityLabel": "Unusual", "evidenceString": "7 sightings on 6 sources including: @Racco42, @romonlyht, hackernoon, @SpamAuditor, @MalwareConfig. Most recent tweet: Hey @CenturyLink, is 204.xx.10.xx/24 assigned to  with no SWIP/rwhois? Full of xxxxname[.]com hostnames, detected of sending #spam. Most recent link (Dec 26, 2019): https://xxxxxx.com/SpamAuditor/statuses/1210333189077495808", "rule": "Historically Reported as a Defanged DNS Name", "criticality": 1}, {"mitigationString": "", "timestamp": "2020-09-01T09:26:47.879Z", "criticalityLabel": "Unusual", "evidenceString": "23 sightings on 4 sources: BTCare Community Forum, Scammedby Scam email, AbuseIP Database, thethreatreport.com. Most recent link (Sep 1, 2020): https://www.abuseipdb.com/check/172.xx.xx.15", "rule": "Historically Linked to Cyber Attack", "criticality": 1}, {"mitigationString": "", "timestamp": "2019-10-24T00:00:00.000Z", "criticalityLabel": "Unusual", "evidenceString": "5 sightings on 1 source: Insikt Group. 5 reports including New B3hpy Malware Linked to Gaza Hacker Team Surfaces Late September 2019 (Oct 24, 2019). Most recent link: https://app.recordedfuture.com/live/sc/xxxx.", "rule": "Historically Referenced by Insikt Group", "criticality": 1}, {"mitigationString": "", "timestamp": "2020-11-18T18:10:09.392Z", "criticalityLabel": "Unusual", "evidenceString": "1 sighting on 1 source: Recorded Future Analyst Community Trending Indicators. Recently viewed by many analysts in many organizations in the Recorded Future community.", "rule": "Trending in Recorded Future Analyst Community", "criticality": 1}], "riskString": "5/47", "rules": 5, "criticality": 1, "riskSummary": "5 of 47 Risk Rules currently observed."}}}, {"Entity": "namexxxx.com", "EntityResult": {"relatedEntities": [{"type": "RelatedMalwareCategory", "entities": [{"count": 2757, "entity": {"id": "0eXxxx", "name": "Computer Worm", "type": "MalwareCategory"}}, {"count": 766, "entity": {"id": "0fLxxx", "name": "Adware", "type": "MalwareCategory"}}]}], "timestamps": {"firstSeen": "2009-03-16T07:21:39.000Z", "lastSeen": "2020-11-18T18:04:19.560Z"}, "intelCard": "https://app.recordedfuture.com/live/sc/entity/idn%3namexxxx.com", "risk": {"criticalityLabel": "Unusual", "score": 15, "evidenceDetails": [{"mitigationString": "", "timestamp": "2020-08-25T20:53:15.451Z", "criticalityLabel": "Unusual", "evidenceString": "9 sightings on 1 source: AbuseIP Database. Most recent link (Aug 25, 2020): https://www.abuseipdb.com/check/17.xx.xx.19", "rule": "Historically Linked to Cyber Attack", "criticality": 1}, {"mitigationString": "", "timestamp": "2020-11-18T18:08:08.367Z", "criticalityLabel": "Unusual", "evidenceString": "Previous sightings on 2 sources: Recorded Future Recent DDNS Names, Recorded Future Analyst Community Trending Indicators. Observed between Sep 8, 2019, and Apr 8, 2020.", "rule": "Historically Reported in Threat List", "criticality": 1}], "riskString": "2/47", "rules": 2, "criticality": 1, "riskSummary": "2 of 47 Risk Rules currently observed."}}}]
```



#### Get Alert Details
Fetch information about specific Alert and return results to the case. Use action to get more information available regarding Recorded Future Alerts - Documents, Related Entities, Evidence, etc...
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert for which you would like to fetch details|True|String||



##### JSON Results
```json
{"data": {"review": {"assignee": null, "noteAuthor": null, "note": null, "status": "no-action", "noteDate": null}, "entities": [{"entity": {"id": "idn:gmaxx.com.xxxsepehlxxx.com", "name": "gmaxx.com.xxxsepehlexxx.com", "type": "InternetDomainName"}, "risk": {"criticalityLabel": "Suspicious", "score": null, "documents": [{"references": [{"fragment": "A certificate for the domain gmail.com.sabsepehlelic.com has been registered", "entities": [{"id": "idn:gmaxx.com.xxxsepehlxxx.com", "name": "gmaxx.com.xxxsepehlexxx.com", "type": "InternetDomainName"}], "language": "eng"}], "source": {"id": "xxx_4-", "name": "New Certificate Registrations", "type": "Source"}, "url": null, "title": "Certificate Registration"}], "evidence": [{"mitigationString": "", "timestamp": "2020-09-28T02:36:23.924Z", "criticalityLabel": "Suspicious", "evidenceString": "1 sighting on 1 source: New Certificate Registrations. Certificate registered on Sep 28, 2020.", "rule": "Newly Registered Certificate With Potential for Abuse - DNS Sandwich", "criticality": 2}, {"mitigationString": "", "timestamp": "2020-09-28T02:36:25.000Z", "criticalityLabel": "Suspicious", "evidenceString": "Identified by Recorded Future as potential typosquatting: DNS Sandwich similarity found between gmail.com.sabsepehlelic.com and 1 possible target: gmail.com.", "rule": "Recent Typosquat Similarity - DNS Sandwich", "criticality": 2}], "criticality": 2}, "trend": {}, "documents": []}, {"entity": {"id": "idn:www.xxail.com.xxxsepehxxxx.com", "name": "www.xxail.com.xxxsepehxxxx.com", "type": "InternetDomainName"}, "risk": {"criticalityLabel": "Suspicious", "score": null, "documents": [{"references": [{"fragment": "A certificate for the domain www.xxail.com.xxxsepehxxxx.com has been registered", "entities": [{"id": "idn:www.xxail.com.xxxsepehxxxx.com", "name": "www.xxail.com.xxxsepehxxxx.com", "type": "InternetDomainName"}], "language": "eng"}], "source": {"id": "xxx_4-", "name": "New Certificate Registrations", "type": "Source"}, "url": null, "title": "Certificate Registration"}], "evidence": [{"mitigationString": "", "timestamp": "2020-09-28T02:36:23.924Z", "criticalityLabel": "Suspicious", "evidenceString": "1 sighting on 1 source: New Certificate Registrations. Certificate registered on Sep 28, 2020.", "rule": "Newly Registered Certificate With Potential for Abuse - DNS Sandwich", "criticality": 2}, {"mitigationString": "", "timestamp": "2020-09-28T02:36:25.000Z", "criticalityLabel": "Suspicious", "evidenceString": "Identified by Recorded Future as potential typosquatting: DNS Sandwich similarity found between www.xxail.com.xxxsepehxxxx.com and 1 possible target: gmail.com.", "rule": "Recent Typosquat Similarity - DNS Sandwich", "criticality": 2}], "criticality": 2}, "trend": {}, "documents": []}], "url": "https://xxx.xxxxedfutxxxx.com/live/sc/notification/?id=feRxxx", "rule": {"url": "https://xxx.xxxxedfutxxxx.com/live/sc/ViewIdkobra_view_report_item_alert_editor?view_opts=%7B%22reportId%22%3A%22eOFFb0%22%2C%22bTitle%22%3Atrue%2C%22title%22%3A%22Infrastructure+and+Brand+Risk%2C+Potential+Typosquatting+Watch+List+Domains%22%7D&state.bNavbar=false", "name": "Infrastructure and Brand Risk, Potential Typosquatting Watch List Domains", "id": "eOFxxx"}, "triggered": "2020-09-28T10:13:40.466Z", "id": "feRxxx", "counts": {"references": 2, "entities": 2, "documents": 1}, "title": "Infrastructure and Brand Risk, Potential Typosquatting Watch List Domains ...", "type": "ENTITY"}}
```



#### Enrich URL
Query the RecordedFuture to get more information about the URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Represents the minimum malicious risk score for a URL to be marked malicious. Has a range of 0-99. Below is the band levels:  Very Malicious: 90-99  Malicious: 65-89  Suspicious: 25-64  Unusual: 5-24  No Malicious content: 0|True|String|25|
|Include Related Entities|If enabled, action will get information about related entities.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "https://www.youtube.com/", "EntityResult": {"relatedEntities": [], "timestamps": {"firstSeen": "2020-11-17T00:00:00.000Z", "lastSeen": "2020-11-17T23:59:59.000Z"}, "risk": {"criticalityLabel": "Unusual", "score": 24, "evidenceDetails": [{"mitigationString": "", "timestamp": "2020-03-02T16:22:27.000Z", "criticalityLabel": "Unusual", "evidenceString": "22 sightings on 14 sources including: @romonlyht, Geeks To Go, Smart Italia, @malwrhunterteam. Most recent tweet: @James_inthe_box @VirITeXplorer @sugimu_sec @58_5_17_102 @JAMESWT_MHT @arturodicorinto @CertPa @reecdeep @0xFrost @merlos1977 @pmelson hxxps://45.4.4.14/C821al/vc2Tmy.php https://t.co/4MVUPgdLOD. Most recent link (Mar 2, 2020): https://twitter.com/Ledtech3/statuses/1234457540614", "rule": "Historically Reported as a Defanged URL", "criticality": 1}, {"mitigationString": "", "timestamp": "2020-07-20T00:00:00.000Z", "criticalityLabel": "Unusual", "evidenceString": "1 sighting on 1 source: URLScan Web Page Analysis. Brand-related image detected on site. Target: UNKNOWN. Last observed on Jul 20, 2020.", "rule": "Historically Detected Phishing Techniques", "criticality": 1}], "riskString": "2/25", "rules": 2, "criticality": 1, "riskSummary": "2 of 25 Risk Rules currently observed."}}}, {"Entity": "https://www.google.com/", "EntityResult": {"relatedEntities": [], "timestamps": {"firstSeen": "2020-11-13T00:00:00.000Z", "lastSeen": "2020-11-13T23:59:59.000Z"}, "risk": {"criticalityLabel": "Unusual", "score": 24, "evidenceDetails": [{"mitigationString": "", "timestamp": "2020-10-06T11:35:50.000Z", "criticalityLabel": "Unusual", "evidenceString": "265 sightings on 48 sources including: @p5yb34m, @akawombat42, urlscan.io, @ScarletSharkSec, @anonimcoder. Most recent tweet: RT @James_inthe_box: @smica83 @JAMESWT_MHT @malwrhunterteam Links hit: https://hacemosmarketingdigital[.]com[.]ar/6bbbktc.php https://heima\u2026. Most recent link (Oct 6, 2020): https://twitter.com/JAMESWT_MHT/statuses/13134428534144", "rule": "Historically Reported as a Defanged URL", "criticality": 1}, {"mitigationString": "", "timestamp": "2020-10-16T00:00:00.000Z", "criticalityLabel": "Unusual", "evidenceString": "1 sighting on 1 source: URLScan Web Page Analysis. Brand-related image detected on site. Target: Excel / PDF download. IP: 2a00:10:41:19::04. Country: DE. Most recent link (Oct 16, 2020): https://urlscan.io/result/a43xxec0-d574-xxxx-bea5-abxxd45xxc61/.", "rule": "Historically Detected Phishing Techniques", "criticality": 1}], "riskString": "2/25", "rules": 2, "criticality": 1, "riskSummary": "2 of 25 Risk Rules currently observed."}}}]
```



#### Get Hash Related Entities
Query the RecordedFuture to get related entities for the Hash.
Timeout - 600 Seconds



#### Update Alert
Update alert in Recorded Future.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert that needs to be updated.|True|String||
|Assign To|Specify to whom to assign the alert. You can provide id, username, user hash, or email.|False|String||
|Note|Specify a note that should be updated on the alert.|False|String||
|Status|Specify the new status for the alert.|True|List|Select One|



##### JSON Results
```json
[{"id": "jU2F_w", "status": "tuning", "assignee": "3NgaozZRYw", "note": {"text": "testing", "author": "3CvPUmFtSX", "date": "2021-08-09T11:21:16Z"}, "reviewDate": "2021-08-09T11:20:31Z"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Get Ip Related Entities
Query the RecordedFuture to get related entities for the IP address.
Timeout - 600 Seconds



#### Get Host Related Entities
Query the RecordedFuture to get related entities for the Host.
Timeout - 600 Seconds









## Connectors
#### Recorded Future - Security Alerts Connector
Pull security alerts from Recorded Future. 
Whitelist and blacklist work with Recorded Future rule names.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|title|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|id|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API URL|API Root of the Recorded Future instance.|True|String|https://api.recordedfuture.com|
|API Key|API Key of the Recorded Future.|True|Password|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Integer|100|
|Severity|Severity will be one from the following values Low, Medium, High, Critical. Will be assigned to Siemplify alerts created from this connector.|True|String|Medium|
|Get Alert's Details|Get alert's full details from Recorded Future. Note: each query "costs" 1 Recorded Future API credit.|False|Boolean|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Recorded Future server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




