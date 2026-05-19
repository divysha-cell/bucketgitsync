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
|AnomaliThreatStream_Ping_1|Test connectivity to the Anomali ThreatStream with parameters provided at the integration configuration page on the Marketplace tab.|AnomaliThreatStream|Ping|
|Siemplify_Add Entity Insight_2|Add an insight configurable message to each targeted entity|Siemplify|Add Entity Insight|
|Siemplify_Case Tag_1|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Siemplify_Add General Insight_1|Add a general insight configurable message to the case|Siemplify|Add General Insight|
|Siemplify_Add Entity Insight_1|Add an insight configurable message to each targeted entity|Siemplify|Add Entity Insight|

### Involved Blocks
|Name|Description|
|----|-----------|
|New Block|An embedded workflow that can receive inputs and return an output.|
