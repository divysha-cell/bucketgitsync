<p align="center"><img src="./Resources/Alexa.svg" 
     alt="Alexa" width="200"/></p>

# Alexa

The Alexa Web Information Service (AWIS) offers a platform for creating innovative Web solutions and services based on Alexa's vast information about web sites.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Access key id|None|True|String||
|Secret access key|None|True|Password|*****|


#### Dependencies
| |
|-|
|defusedxml-0.7.1-py2.py3-none-any.whl|


## Actions
#### Get URL Rank
Query Alexa for URL rank information
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Rank. e.g. 5|True|String||



##### JSON Results
```json
[{"EntityResult": {"TrafficData": [{"text": "          ", "DataUrl": [{"text": "domain.com", "type": "canonical"}], "Rank": [{"text": "5"}]}], "text": "        ", "Request": [{"text": "          ", "Arguments": [{"text": "            ", "Argument": [{"text": "              ", "Name": [{"text": "url"}], "Value": [{"text": "domain.com"}]}, {"text": "              ", "Name": [{"text": "responsegroup"}], "Value": [{"text": "Rank"}]}]}]}]}, "Entity": "domain.com"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









