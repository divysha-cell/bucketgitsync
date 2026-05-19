# AWS User Containment
This block allows you to disable access for users referenced in the case, supporting containment actions during the incident response process. It uses a boolean input to control manual or automatic execution and returns the containment result, false on failure, or an empty value if no action is taken.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False



##### Input Parameters
|Name|Default Value|
|----|-------------|
|Manual|True|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Count User Accounts|Count the number of entities from a specific scope.|SiemplifyUtilities|Count Entities In Scope|
|Auto Disable Users Access|Disable User Access in AWS by adding an explicit deny inline policy. Action works with SOAR User entity type.|AWSIAM|Disable User Access|
|Disable Users Access|Disable User Access in AWS by adding an explicit deny inline policy. Action works with SOAR User entity type.|AWSIAM|Disable User Access|

