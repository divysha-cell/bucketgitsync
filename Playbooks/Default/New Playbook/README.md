# New Playbook




**Enabled:** True

**Version:** 1

**Type:** Playbook

**Priority:** 2

**Playbook Simulator:** False



### Playbook Trigger
**Trigger Type:** All

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
||Equals||



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Siemplify_Case Tag_1|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Lists_Ping_1|Check connectivity|Lists|Ping|

### Involved Blocks
|Name|Description|
|----|-----------|
|Alert Prioritization|This blocks changes the alert priority value based on the alert score.|
|New Block|An embedded workflow that can receive inputs and return an output.|
