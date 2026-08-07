
# ThreatConnect

An integration utilizing the ThreatConnect v3 REST API to manage and enrich threat intelligence indicators.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The base URL of the ThreatConnect API instance.|True|String|https://partners.threatconnect.com/api|
|API Access ID|The Unique Access ID generated from the ThreatConnect platform.|True|String||
|API Secret Key|The Secret Key associated with the Access ID.|True|Password|*****|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to the server. Selected by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|httplib2-0.31.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pyzipper-0.4.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|googleapis_common_protos-1.75.0-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|protobuf-7.34.1-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|urllib3-1.26.20-py2.py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|h11-0.16.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pycryptodomex-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|TIPCommon-2.3.8-py3-none-any.whl|


## Actions
#### Execute HTTP Request
Use the Execute HTTP Request action to construct and execute a customized HTTP API request against a target URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Method|The HTTP method (verb) used for the request.|True|List|GET|
|URL Path|The API endpoint where the request executes.|True|String|https://|
|URL Params|Query parameters for the URL, provided as a JSON object.|False|String|None|
|Headers|Headers for the HTTP request, specified as a JSON object.|False|String|None|
|Cookie|Cookies constructed into the HTTP Cookie header, specified as a JSON object.|False|String|None|
|Body Payload|The content payload for the HTTP request.|False|String|None|
|Expected Response Values|JSON object defining the required successful state. Triggers async mode.|False|String|None|
|Follow Redirects|If selected, automatically follows HTTP redirect responses.|False|Boolean|true|
|Fail on HTTP Error|If selected, explicitly fails the step on 4xx or 5xx status codes.|False|Boolean|true|
|Base64 Output|If selected, converts the entire HTTP response body to a Base64 encoded string.|False|Boolean|false|
|Fields To Return|Comma-separated list of fields to return in the output.|True|String|response_data, redirects, response_code, response_cookies, response_headers, apparent_encoding|
|Request Timeout|The maximum time, in seconds, the action waits for the server to send data.|True|String|120|
|Save To Case Wall|If selected, saves the file and attaches it to the case wall as a ZIP.|False|Boolean|false|
|Password Protect Zip|If enabled, action will add an "infected" password to the zip created with "Save To Case Wall" parameter. Use this, when you are dealing with suspicious files.|False|Boolean|true|



##### JSON Results
```json
{"response_data": null, "redirects": ["https://sandbox.threatconnect.com/api"], "response_code": 200, "response_cookies": {}, "response_headers": {}, "apparent_encoding": "utf-8"}
```



#### Enrich Entities
Enrich IP addresses, hosts, URLs and hashes with information from ThreatConnect
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Owner Name|Owner name to fetch the data from. Parameter also accepts comma separated list of owner names.|False|String|None|



##### JSON Results
```json
[{"Entity": "HTTP://MARKOSSOLOMON.COM/F1Q7QX.PHP", "EntityResult": {"attributes": {"Description": ["URLAssociatedwithCryptoLockerC2Servers"]}, "general": {"url": {"confidence": 100, "dateAdded": "2018-01-09T20:12:11Z", "description": "URLAssociatedwithCryptoLockerC2Servers", "id": 43743075, "lastModified": "2018-01-09T20:13:24Z", "owner": {"id": 440, "name": "S", "type": "Organization"}, "rating": 5.0, "text": "http://markossolomon.com/f1q7qx.php", "threatAssessConfidence": 93.33, "threatAssessRating": 4.33, "webLink": "https://sandbox.threatconnect.com/auth/indicators/details/url.xhtml?orgid=43743075&owner=S"}}, "groups": null, "indicators": {"indicator": [], "resultCount": 0}, "observationCount": {"observationCount": {"count": 0}}, "observations": {"observation": [], "resultCount": 0}, "owners": {"owner": [{"id": 440, "name": "S", "type": "Organization"}]}, "securityLabels": {"resultCount": 0, "securityLabel": []}, "tags": ["C2", "Malware"], "victimAssets": {"resultCount": 0, "victimAsset": []}, "victims": {"resultCount": 0, "victim": []}}}]
```



#### Ping
Use the Ping action to test the connectivity to the ThreatConnect platform.
Timeout - 600 Seconds









