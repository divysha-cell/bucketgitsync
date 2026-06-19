# Connector_28_Gmail
The Gmail Connector retrieves Gmail emails from the specified mailbox. To filter specific values from the email body and subject, use the dynamic list regular expressions in the following format: “key: regex”. For example, after finding a match for the following regex: “subject: (?<=Subject: ).*”, the connector creates a Google SecOps alert event and adds a new key with the “subject” name to it. The new key value matches the regular expression.


Integration: Gmail

Integration Version: 9

Device Product Field: device_product

Event Name Field: event_name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored.
If the environment field isn't found, the environment is the default environment.
|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.
Default is .* to catch all and return the value unchanged.
Used to allow the user to manipulate the environment field via regex logic.
If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|dummy_valid_string|
|Email Exclude Pattern|A regular expression to exclude specific emails from ingestion, such as spam or news. This parameter works with both the subject and the body of an email. For example, to exclude the autoreply emails from ingestion, you can configure the following regular expression: (?i)(auto|no)(\s|-)?re(ply|sponse|sponder)|False|dummy_valid_string|
|Service Account JSON File Content|The content of the service account key JSON file. You can configure either this parameter or the Workload Identity Email parameter. To configure this parameter, provide the full content of the service account key JSON file that you have downloaded when creating a service account.|False|*****|
|Workload Identity Email|The client email address of your service account.
You can configure either this parameter or the Service Account JSON File Content parameter. To impersonate service accounts with workloads, grant the Service Account Token Creator role to your Google SecOps service account.|False|dummy_valid_string|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation.
Not selected by default.
|False|false|
|Default Mailbox|An email address to use as a default mailbox for the integration, such as user@example.com.|True|dummy_valid_string|
|Labels Filter|The labels of emails to ingest into Google SecOps. The connector supports nested labels. Provide the labels in a format that is acceptable for Gmail, such as Inbox-label1-label2.|False|Inbox|
|Email Status|A status of the email to search for. Possible values are as follows: Both, Read, Unread. The default value is Both.|False|Both|
|Mark Emails as Read|If selected, the connector marks ingested emails as read.|False|true|
|Extract Headers|Header values to filter from the “internetMessageHeaders” list and add to a Google SecOps event. By default, the connector adds all headers to the event. To add only specific headers, enter them as a comma-separated list, such as “DKIM-Siganture”, “Received”, “From”. To prevent the connector from adding any header, enter the following value: None. This parameter is case-insensitive.|False|dummy_valid_string|
|Attached Mail File Prefix|A prefix to add to the extracted event keys (for example, to, from, or subject) from the attached email file received in the monitored mailbox.|False|attach|
|Original Mail File Prefix|A prefix to add to the extracted event keys (for example, to, from, or subject) from the original email received in the monitored mailbox.|False|orig|
|Attach Original EML|If selected, the connector attaches the original email to the case information as an EML file.
Not selected by default.
|False|false|
|Create Alert Per Attachment File|If selected, the connector creates multiple alerts, with one alert for every attached email file.
This behavior is useful when you process emails with multiple email files attached and set the Google SecOps event mapping to create entities from attached email files.
Not selected by default.|False|false|
|Max Emails Per Cycle|The maximum number of emails to retrieve for every connector iteration.
The maximum number is 100 emails. The default value is 10 emails.|True|10|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp.|True|24|
|Case Name Template|A custom case name. When you configure this parameter, the connector adds a new key called custom_case_name to the Google SecOps event. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. For placeholders, the connector uses the first Google SecOps event. The connector only handles keys that contain the string value. To configure this parameter, specify event fields without prefixes.|False|dummy_valid_string|
|Alert Name Template|A custom alert name. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. For placeholders, the connector uses the first Google SecOps event. The connector only handles keys containing the string value. If you don’t provide any value or use an invalid template, the connector uses the default alert name. To configure this parameter, specify event fields without prefixes.|False|dummy_valid_string|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Gmail server is valid.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|

