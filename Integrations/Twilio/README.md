
# Twilio

Twilio provides a link between the internet and telecom networks. Use Twilio for voice and messaging features

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|AccountSid||True|String|None|
|AuthenticationToken||True|Password|*****|
|SmsPhoneNumber||True|String||


#### Dependencies
| |
|-|
|certifi-2026.5.20-py3-none-any.whl|
|twilio-9.2.4-py2.py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|yarl-1.24.2-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|pyjwt-2.13.0-py3-none-any.whl|
|idna-3.16-py3-none-any.whl|
|attrs-26.1.0-py3-none-any.whl|
|aiohttp_retry-2.9.1-py3-none-any.whl|
|aiosignal-1.4.0-py3-none-any.whl|
|frozenlist-1.8.0-cp311-cp311-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl|
|aiohttp-3.13.5-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|propcache-0.5.2-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|aiohappyeyeballs-2.6.2-py3-none-any.whl|
|multidict-6.7.1-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|


## Actions
#### Send SMS
Send SMS
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Phone Number|Target phone number.The phone number must include a dial code.|True|String||
|Message|Message content.|True|String|Testing|



#### Send SMS And Wait
Send SMS and wait for answer. The message will be sent with a generated SiemplifyID: <code>. The action will wait for a response containing SiemplifyID: <code>.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Phone Number|Target phone number.The phone number must include a dial code.|True|String||
|Message|Message content.|True|String||



#### Ping
Test Connectivity
Timeout - 600 Seconds









