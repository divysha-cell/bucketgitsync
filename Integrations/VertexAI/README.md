
# VertexAI

Vertex AI is a fully-managed, unified AI development platform for building and using generative AI.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API Root of the Vertex AI integration.|True|String|https://{location}-aiplatform.googleapis.com|
|Workload Identity Email|The client email address of your workload identity. You can configure either this parameter or the Service Account Json File Content parameter. To impersonate service accounts with the workload identity email address, grant the Service Account Token Creator role to your service account.|False|String||
|Service Account Json File Content|The content of the service account key JSON file. You can configure either this parameter or the Workload Identity Email parameter. To configure this parameter, provide the full content of the service account key JSON file that you downloaded when creating a service account.|False|Password|*****|
|Project ID|The project ID to use in the integration. If you don't set a value for this parameter, the integration retrieves the project ID from your Google Cloud service account.|False|String||
|Location ID|The location ID to use in generative API calls.|False|String||
|Default Model|The name of the default model to use in the integration.|True|String|gemini-2.0-flash-lite|
|Publisher Name|The name of the default publisher for the model.|True|String|google|
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to Vertex AI is valid. Selected by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|cross/proto_plus-1.25.0-py3-none-any.whl|
|cross/uritemplate-4.1.1-py2.py3-none-any.whl|
|cross/httpx-0.27.2-py3-none-any.whl|
|cross/h11-0.14.0-py3-none-any.whl|
|cross/httplib2-0.22.0-py3-none-any.whl|
|cross/protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|cross/anyio-4.6.2.post1-py3-none-any.whl|
|cross/google_auth-2.36.0-py2.py3-none-any.whl|
|cross/urllib3-2.2.3-py3-none-any.whl|
|cross/pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|cross/requests-2.32.3-py3-none-any.whl|
|cross/TIPCommon-2.2.1-py2.py3-none-any.whl|
|cross/idna-3.10-py3-none-any.whl|
|cross/EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cross/httpcore-1.0.6-py3-none-any.whl|
|cross/pyparsing-3.2.0-py3-none-any.whl|
|cross/charset_normalizer-3.4.0-py3-none-any.whl|
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
#### Describe Entity
Preview. Use the Describe Entity action to summarize information about entities using Vertex AI. This action works with all entity types. and submits every entity individually.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Model ID|The ID of the model to use, such as gemini-1.5-flash-002.|False|String||
|Publisher Name|The name of the publisher for the model.|False|String||
|Temperature|The value to control the degree of randomness in a token selection. This parameter accepts float data type values. For more information about temperature values, see "Experiment with the parameter values" (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#temperature).|False|String||
|Exclude Fields|A comma-separated list of the Google SecOps entity metadata fields to exclude during the entity summary generation.|False|String||
|Force Refresh|If selected, the action ignores the "Refresh After (Days)" parameter and hash validation and regenerates the entity summary for every action run.|False|Boolean|False|
|Refresh After (Days)|The number of days for the action to wait before refreshing the entity summary. The action generates a hash value that is based on all inputs that are sent to Vertex AI excluding values from the "Fields To Ignore" parameter. If the hash value changed, the action refreshes the summary after the set number of days. If the hash value didn’t change, the action doesn’t refresh the summary even if the "Refresh After (Days)" parameter value is earlier than the latest summary generation time. The action validates the hash value of the latest actual generated summary and ignores the cached hash value.|True|String|30|
|Max Output Tokens|The maximum number of output tokens to generate in every response. A token is approximately four characters. 100 tokens correspond to roughly 60-80 words. This limit applies to every individual entity. For more information, see "Experiment with parameter values" (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#max-output-tokens).|False|String||



##### JSON Results
```json
[{"Entity": "lab@siemplify.local", "EntityResult": {"summary": "Hostname LAB@SIEMPLIFY.LOCAL, external, not suspicious, created automatically, associated with IP address 10.0.0.28 and user XWZNR1L@GMAIL.COM.\n", "usageMetadata": {"promptTokenCount": 64, "candidatesTokenCount": 45, "totalTokenCount": 109}}}, {"Entity": "10.0.0.28", "EntityResult": {"summary": "IP address 10.0.0.28, external, not suspicious, found in Default Environment, automatically detected, associated with hostname LAB@SIEMPLIFY.LOCAL.\n", "usageMetadata": {"promptTokenCount": 64, "candidatesTokenCount": 38, "totalTokenCount": 102}}}, {"Entity": "XWZNR1L@GMAIL.COM", "EntityResult": {"summary": "Email address XWZNR1L@GMAIL.COM, a non-internal, non-suspicious user account, was automatically created in the Default Environment and is associated with the hostname LAB@SIEMPLIFY.LOCAL.  It is not from an LDAP string.\n", "usageMetadata": {"promptTokenCount": 64, "candidatesTokenCount": 56, "totalTokenCount": 120}}}, {"Entity": "USB_DEVICE_1", "EntityResult": {"summary": "USB device USB_DEVICE_1, internal, not suspicious, automatically created in the Default Environment.  No related entities or source URL.\n", "usageMetadata": {"promptTokenCount": 64, "candidatesTokenCount": 29, "totalTokenCount": 93}}}]
```



#### Transform Data
Preview. Use the Transform Data action to perform data transformations using Vertex AI.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Model ID|The ID of the model to use, such as gemini-1.5-flash-002.|False|String||
|Publisher Name|The name of the publisher for the model.|False|String||
|Text Prompt|The text instructions to include in the prompt.|True|String||
|Temperature|The value to control the degree of randomness in a token selection. This parameter accepts float data type values. For more information about temperature values, see “Experiment with the parameter values” (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#temperature).|False|String||
|JSON Object|The JSON object to use as an action input.|True|String||
|Max Output Tokens|The maximum number of output tokens to generate in every response. A token is approximately four characters. 100 tokens correspond to roughly 60-80 words. For more information, see “Experiment with parameter values” (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#max-output-tokens).|True|String|100|



##### JSON Results
```json
{"candidates":[{"content":{"role":"model","parts":[{"text":"{\"key\": \"value\", \"key1_key3\": \"value1\"}"}]},"finishReason":"STOP","avgLogprobs":-0.004595317384775947}],"usageMetadata":{"promptTokenCount":7,"candidatesTokenCount":17,"totalTokenCount":24},"modelVersion":"gemini-1.5-flash-002","text_content":"{\"key\": \"value\", \"key1_key3\": \"value1\"}","extracted_info":{"key":"value","key1_key3":"value1"}}
```



#### Execute Prompt
Use the Execute Prompt action to execute individual text prompts using Vertex AI.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Model ID|The ID of the model to use, such as gemini-1.5-flash-002.|False|String||
|Publisher Name|The name of the publisher for the model.|False|String||
|Text Prompt|The text instructions to include in the prompt.|True|String||
|Temperature|The value to control the degree of randomness in a token selection. This parameter accepts float data type values. For more information about temperature values, see "Experiment with the parameter values" (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#temperature).|False|String||
|Candidate Count|The number of response variations to return in every action run. For every request, the billing applies to an input token once and every output token of all generated candidates.|False|String||
|Response MIME type|The media (MIME) type of the output response for the generated candidate text. The response media (MIME) type is available for the following models: gemini-1.5-pro, gemini-1.5-flash.|False|List|text/plain|
|Response Schema|The schema for the generated candidate text to follow. To use this parameter, configure the "Response mIME Type" parameter. The response schema is available for the following models: gemini-1.5-pro, gemini-1.5-flash.|False|String||
|Max Input Tokens|The maximum number of input tokens to submit. One token consists of up to four characters. 100 tokens can correspond to 60-80 words. If you don’t set a value, the action executes any prompt. If the number of tokens exceeds the configured maximum number, the action fails.|False|String||
|Max Output Tokens|The maximum number of output tokens to generate in every response. A token is approximately four characters. 100 tokens correspond to roughly 60-80 words. For more information, see "Experiment with parameter values" (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#max-output-tokens).|False|String||



##### JSON Results
```json
{"candidates": [{"content": {"role": "model", "parts": [{"text": "Protecting your Gmail mailbox from phishing attempts requires a multi-layered approach. Here's a breakdown of effective strategies:\n\n**1. Strong Password and Two-Factor Authentication (2FA):**\n\n* **Strong Password:**  Use a long, complex password that combines uppercase and lowercase letters, numbers, and symbols. Avoid using easily guessable information like your name, birthday, or pet's name.  Consider a password manager to generate and securely store strong, unique passwords.\n* **Two-Factor Authentication (2FA):**  This is arguably the single most important step.  2FA adds an extra layer of security by requiring a second verification method (like a code from your phone or a security key) in addition to your password. Enable 2FA in your Google account settings.  Choose a method you'll reliably have access to.\n\n**2. Be Vigilant and Recognize Phishing Attempts:**\n\n* **Suspicious Emails:**  Look for red flags like:\n    * **Generic greetings:**  Emails that address you as \"Dear Customer\" or \"Valued User\" instead of your name.\n    * **Urgent or threatening language:**  Phishing emails often try to create a sense of urgency to pressure you into acting quickly.\n    * **Suspicious links:**  Hover your mouse over links (without clicking) to see the actual URL.  Does it match the expected domain?  Be wary of shortened URLs.\n    * **Grammar and spelling errors:**  Phishing emails often contain grammatical errors or poor spelling.\n    * **Unexpected attachments:**  Don't open attachments from unknown senders, even if they appear to be from a legitimate source.\n    * **Requests for personal information:**  Legitimate companies rarely ask for your password, credit card details, or other sensitive information via email.\n    * **Unusual email addresses:**  Check the sender's email address carefully.  Look for slight variations in the domain name (e.g., googl3.com instead of google.com).\n\n* **Suspicious websites:**  If you're unsure about a website's legitimacy, search online for reviews or look for security indicators like \"https\" in the URL and a padlock icon in the address bar.\n\n**3. Utilize Gmail's Security Features:**\n\n* **Gmail's Phishing and Malware Protection:** Gmail's built-in filters are effective at blocking many phishing emails, but they're not foolproof.\n* **Suspicious Activity Alerts:** Enable Gmail's security alerts to receive notifications about suspicious login attempts or changes to your account.\n* **Google Account Security Checkup:** Regularly perform a security checkup in your Google account settings.  This will guide you through reviewing your security settings and identify potential vulnerabilities.\n* **Advanced Protection Program:** If you're a high-profile target, consider Google's Advanced Protection Program, which provides an even higher level of security.\n\n**4. Keep Software Updated:**\n\n* **Operating System:** Keep your operating system and applications updated with the latest security patches.\n* **Antivirus Software:** Use a reputable antivirus program on your computer and mobile devices.\n\n**5. Education and Awareness:**\n\n* **Stay Informed:**  Regularly read articles and resources about phishing scams to stay aware of the latest techniques.\n* **Train Others:**  If you share a computer or network with others, educate them about phishing awareness.\n\n\nBy implementing these measures, you significantly reduce your risk of falling victim to phishing attempts targeting your Gmail account. Remember that vigilance and a healthy dose of skepticism are your best defenses.  If you suspect you've received a phishing email, report it to Gmail and don't click on any links or attachments.\n"}]}, "finishReason": "STOP", "avgLogprobs": -0.22686134945149528}], "usageMetadata": {"promptTokenCount": 10, "candidatesTokenCount": 767, "totalTokenCount": 777}, "modelVersion": "gemini-1.5-flash-002", "text_content": "Protecting your Gmail mailbox from phishing attempts requires a multi-layered approach. Here's a breakdown of effective strategies:\n\n**1. Strong Password and Two-Factor Authentication (2FA):**\n\n* **Strong Password:**  Use a long, complex password that combines uppercase and lowercase letters, numbers, and symbols. Avoid using easily guessable information like your name, birthday, or pet's name.  Consider a password manager to generate and securely store strong, unique passwords.\n* **Two-Factor Authentication (2FA):**  This is arguably the single most important step.  2FA adds an extra layer of security by requiring a second verification method (like a code from your phone or a security key) in addition to your password. Enable 2FA in your Google account settings.  Choose a method you'll reliably have access to.\n\n**2. Be Vigilant and Recognize Phishing Attempts:**\n\n* **Suspicious Emails:**  Look for red flags like:\n    * **Generic greetings:**  Emails that address you as \"Dear Customer\" or \"Valued User\" instead of your name.\n    * **Urgent or threatening language:**  Phishing emails often try to create a sense of urgency to pressure you into acting quickly.\n    * **Suspicious links:**  Hover your mouse over links (without clicking) to see the actual URL.  Does it match the expected domain?  Be wary of shortened URLs.\n    * **Grammar and spelling errors:**  Phishing emails often contain grammatical errors or poor spelling.\n    * **Unexpected attachments:**  Don't open attachments from unknown senders, even if they appear to be from a legitimate source.\n    * **Requests for personal information:**  Legitimate companies rarely ask for your password, credit card details, or other sensitive information via email.\n    * **Unusual email addresses:**  Check the sender's email address carefully.  Look for slight variations in the domain name (e.g., googl3.com instead of google.com).\n\n* **Suspicious websites:**  If you're unsure about a website's legitimacy, search online for reviews or look for security indicators like \"https\" in the URL and a padlock icon in the address bar.\n\n**3. Utilize Gmail's Security Features:**\n\n* **Gmail's Phishing and Malware Protection:** Gmail's built-in filters are effective at blocking many phishing emails, but they're not foolproof.\n* **Suspicious Activity Alerts:** Enable Gmail's security alerts to receive notifications about suspicious login attempts or changes to your account.\n* **Google Account Security Checkup:** Regularly perform a security checkup in your Google account settings.  This will guide you through reviewing your security settings and identify potential vulnerabilities.\n* **Advanced Protection Program:** If you're a high-profile target, consider Google's Advanced Protection Program, which provides an even higher level of security.\n\n**4. Keep Software Updated:**\n\n* **Operating System:** Keep your operating system and applications updated with the latest security patches.\n* **Antivirus Software:** Use a reputable antivirus program on your computer and mobile devices.\n\n**5. Education and Awareness:**\n\n* **Stay Informed:**  Regularly read articles and resources about phishing scams to stay aware of the latest techniques.\n* **Train Others:**  If you share a computer or network with others, educate them about phishing awareness.\n\n\nBy implementing these measures, you significantly reduce your risk of falling victim to phishing attempts targeting your Gmail account. Remember that vigilance and a healthy dose of skepticism are your best defenses.  If you suspect you've received a phishing email, report it to Gmail and don't click on any links or attachments.\n", "extracted_info": null}
```



#### Analyze EML
Preview. Use the Analyze EML action to analyze EML files using Vertex AI. The action submits every file individually.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Model ID|The ID of the model to use, such as gemini-1.5-flash-002.|False|String||
|Publisher Name|The name of the publisher for the model.|False|String||
|Temperature|The value to control the degree of randomness in a token selection. This parameter accepts float data type values. For more information about temperature values, see “Experiment with the parameter values” (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#temperature).|False|String||
|Files To Analyze|Comma-separated list of EML files to submit for analysis.|True|String||
|Max Output Tokens|The maximum number of output tokens to generate in every response. A token is approximately four characters. 100 tokens correspond to roughly 60-80 words. This limit applies to every individual entry. For more information, see “Experiment with parameter values” (https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/adjust-parameter-values#max-output-tokens).|False|String||



##### JSON Results
```json
[{"Entity":"/tmp/Suspicious.eml","EntityResult":{"raw":"The email promotes PMP training courses via numerous links to yyyy.com. While the email uses DKIM and SPF authentication, the numerous shortened links raise suspicion. These links could lead to phishing sites designed to steal credentials or install malware. The sender's email address (jennifer@domain.com) should be independently verified. Further investigation should involve checking the legitimacy of yyyy.com, analyzing the destination URLs of the shortened links, and checking the domain reputation of domain.com. Users should avoid clicking on links from untrusted sources and only access websites directly through their official address.\n","extracted_info":{"threat_level":"high","threats_found":["Numerous suspicious shortened links","Potential credential theft phishing","Risk of malware installation"],"verification_steps":["Verify sender jennifer@domain.com","Check legitimacy of yyyy.com","Analyze destination of shortened URLs"],"protection_measures":["Do not click links from untrusted sources","Access websites directly via official address"]},"usageMetadata":{"promptTokenCount":12,"candidatesTokenCount":778,"totalTokenCount":790}}}]
```



#### Ping
Use the Ping action to test the connectivity to Vertex AI.
Timeout - 600 Seconds



##### JSON Results
```json

```









