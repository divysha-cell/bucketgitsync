
# Websense

Websense identifies and classifies known and emerging internet security threats to provide protection with software that allows organizations to manage internet access, block malicious code and unwanted applications, and prevent the loss of confidential information.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api root||True|String||
|Gateway host||True|String||
|Gateway user||True|String||
|Gateway password||True|Password|*****|
|Verify SSL||False|Boolean|false|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Block Url API
Block a URL in WebSense API category
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|CategoryName|The API manage category name.|True|String||
|Urls|The URLs to block, comma separated.|False|String||



#### Get Category Urls API
Get a list off all category's URLs
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|CategoryName|The API manage category name|True|String||



#### Ping
Test connectivity to WebSense
Timeout - 600 Seconds



#### Unblock Url API
Unblock URL in WebSense API category
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|CategoryName|The API manage category name.|True|String||
|URL|The url to block.|False|String||









