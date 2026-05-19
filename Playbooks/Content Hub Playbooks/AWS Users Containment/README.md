# AWS Users Containment
An embedded workflow that can receive inputs and return an output.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False



##### Input Parameters
|Name|Default Value|
|----|-------------|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|USER_REMEDIATION_SUMMARY_DENY|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Init Remediation|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|AWSIAM_Disable User Access_1|Disable User Access in AWS by adding an explicit deny inline policy. Action works with SOAR User entity type.|AWSIAM|Disable User Access|
|USER_REMEDIATION_SUMMARY_APRPOVE|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|

