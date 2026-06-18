
# WebRisk

Web Risk is a powerful Google Cloud service that leverages AI and ML to proactively protect your users and your platform from unsafe websites.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API Root of the Web Risk integration.|True|String|https://webrisk.googleapis.com/v1|
|Workload Identity Email|The client email address of your workload identity. You can configure either this parameter or the Service Account Json File Content parameter. To impersonate service accounts with the workload identity email address, grant the Service Account Token Creator role to your service account.|False|String||
|Service Account Json File Content|The content of the service account key JSON file. You can configure either this parameter or the Workload Identity Email parameter. To configure this parameter, provide the full content of the service account key JSON file that you downloaded when creating a service account.|False|Password|*****|
|Quota Project ID|The Google Cloud project ID which you use for Google Cloud APIs and billing. This parameter requires you to grant the Service Usage Consumer role to your service account.The integration attaches this parameter value to all API requests. If you don't set a value for this parameter, the integration retrieves the quota project ID from your Google Cloud service account.|False|String||
|Project ID|The project ID to use in the integration. If you don't set a value for this parameter, the integration retrieves the project ID from your Google Cloud service account.|False|String||
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to Vertex AI is valid. Selected by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|cross/proto_plus-1.25.0-py3-none-any.whl|
|cross/uritemplate-4.1.1-py2.py3-none-any.whl|
|cross/httpx-0.27.2-py3-none-any.whl|
|cross/h11-0.14.0-py3-none-any.whl|
|cross/httplib2-0.22.0-py3-none-any.whl|
|cross/TIPCommon-2.0.7-py2.py3-none-any.whl|
|cross/protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|cross/anyio-4.6.2.post1-py3-none-any.whl|
|cross/google_auth-2.36.0-py2.py3-none-any.whl|
|cross/urllib3-2.2.3-py3-none-any.whl|
|cross/charset_normalizer-3.4.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|cross/requests-2.32.3-py3-none-any.whl|
|cross/idna-3.10-py3-none-any.whl|
|cross/EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cross/httpcore-1.0.6-py3-none-any.whl|
|cross/pyparsing-3.2.0-py3-none-any.whl|
|cross/pyasn1_modules-0.4.1-py3-none-any.whl|
|cross/googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|cross/google_api_core-2.23.0-py3-none-any.whl|
|cross/sniffio-1.3.1-py3-none-any.whl|
|cross/certifi-2024.8.30-py3-none-any.whl|
|cross/rsa-4.9-py3-none-any.whl|
|cross/google_api_python_client-2.151.0-py2.py3-none-any.whl|
|cross/pyasn1-0.6.1-py3-none-any.whl|
|cross/cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Enrich Entities
Use the Enrich Entities action to return information about Google SecOps entities from Web Risk. This action runs on the following Google SecOps entities: URL.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "http://testsafebrowsing.appspot.com/s/malware.html", "EntityResult": {"threatTypes": ["MALWARE"], "expireTime": "2025-02-07T12:24:02.312626714Z"}}]
```



#### Submit Entities
Use the Submit Entities action to submit entities to Web Risk for analysis. This action runs on the Google SecOps URL entity. This action is asynchronous. Adjust the script timeout value in the Google SecOps IDE for the action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Abuse Type|The abuse type that is associated with the submission. For more information about abuse types, see AbuseType (https://cloud.google.com/web-risk/docs/reference/rest/v1/projects.uris/submit#abusetype).|False|List|Select One|
|Confidence Level|The confidence level for the submission. For more information about confidence levels, see Confidence (https://cloud.google.com/web-risk/docs/reference/rest/v1/projects.uris/submit#confidence) and ConfidenceLevel (https://cloud.google.com/web-risk/docs/reference/rest/v1/projects.uris/submit#confidencelevel).|False|List|Select One|
|Justification|The justification for the submission. For more information about justification options, see JustificationLabel (https://cloud.google.com/web-risk/docs/reference/rest/v1/projects.uris/submit#justificationlabel).|False|List|Select One|
|Comment|A comment to explain the submission justification.|False|String||
|Region Code|A comma-separated list of the Common Locale Data Repository (CLDR) codes for countries or regions that associate with the submission. For more information about submissions, see Submission (https://cloud.google.com/web-risk/docs/reference/rest/v1/projects.uris/submit#submission).|False|String||
|Platform|A platform type on which the submission was detected.|False|List|Select One|
|Skip Waiting|If enabled, action will just initialize the submission and not wait for it to be finished.|False|Boolean|false|



##### JSON Results
```json
[{"Entity": "http://testsafebrowsing.appspot.com/s/malware.html", "EntityResult": {"name": "projects/123456789/operations/123456789123456789", "metadata": {"@type": "type.googleapis.com/google.cloud.webrisk.v1.SubmitUriMetadata", "state": "SUCCEEDED", "createTime": "2025-02-07T11:10:48.503573Z", "updateTime": "2025-02-07T11:10:48.503573Z"}, "done": true, "response": {"@type": "type.googleapis.com/google.cloud.webrisk.v1.Submission", "uri": "http://testsafebrowsing.appspot.com/s/malware.html", "threatTypes": ["MALWARE"]}}}]
```



#### Ping
Use the Ping action to test the connectivity to Web Risk.
Timeout - 600 Seconds



##### JSON Results
```json

```









