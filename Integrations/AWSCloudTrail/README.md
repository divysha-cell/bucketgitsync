
# AWSCloudTrail

AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting. In addition, you can use CloudTrail to detect unusual activity in your AWS accounts. These capabilities help simplify operational analysis and troubleshooting.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|AWS Access Key ID||True|String||
|AWS Secret Key||True|Password|*****|
|AWS Default Region||True|String||


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|boto3-1.35.4-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|cryptography-48.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|pyopenssl-26.2.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|botocore-1.35.99-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.7.0-py3-none-any.whl|
|requests-2.34.2-py3-none-any.whl|
|s3transfer-0.10.4-py3-none-any.whl|
|jmespath-1.1.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Ping
Test connectivity to AWS Cloud Trail with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### AWS Cloud Trail - Insights Connector
Pull insights from AWS Cloud Trail.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|AWS Access Key ID|AWS Access Key ID to use in integration.|True|String||
|AWS Secret Key|AWS Secret Key to use in integration.|True|Password|*****|
|AWS Default Region|AWS default region to use in integration, for example us-west-2.|True|String||
|Alert Severity|Severity of the Siemplify Alerts created based on the insights. Possible values: Informational, Low, Medium, High, Critical|True|String|Medium|
|Max Insights To Fetch|How many insights to process per one connector iteration. Maximum is 50.|False|Int|50|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve insights from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the AWS Cloud Trail server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




