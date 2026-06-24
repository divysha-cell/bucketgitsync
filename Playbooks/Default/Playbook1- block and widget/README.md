# Playbook1- block and widget




**Enabled:** True

**Version:** 1

**Type:** Playbook

**Priority:** 1

**Playbook Simulator:** True



### Playbook Trigger
**Trigger Type:** Alert Trigger Value

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
||Equals|tag|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Siemplify_Case Tag_1|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|GitSync_Ping_1|Test connectivity to GitSync|GitSync|Ping|

### Involved Blocks
|Name|Description|
|----|-----------|
|Block1|An embedded workflow that can receive inputs and return an output.|
