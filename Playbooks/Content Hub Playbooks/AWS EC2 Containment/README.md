# AWS EC2 Containment
This block allows the playbook to automatically stop EC2 instances that were identified in the alert as potentially compromised or suspicious, supporting the containment phase of the incident response process.



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
|AWSEC2 Stop Instance|Stop an Amazon EBS-backed instance. When you stop an instance, we attempt to shut it down forcibly after a short while. It can take a few minutes for the instance to stop. The instance can be started at any time. Notice that you can't stop an instance store-backed instance.  For more information about instance store-backed instances, see https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ComponentsAMIs.html#storage-for-the-root-device|AWSEC2|Stop Instance|
|Instance Ids|This action includes basic Pythonic string functions as mentioned below - Lower: Converts the input string to lowercase.Upper: Converts the input string to uppercase (duplicated case in the script).Strip: Removes leading and trailing whitespaces from the input string.Title: Converts the first character of each word in the input string to uppercase.Count: Counts the occurrences of `param_1` in the input string.Replace: Replaces occurrences of `param_1` with `param_2` in the input string.Find: Finds the first occurrence of `param_1` in the input string and returns its index.IsAlpha: Checks if all characters in the input string are alphanumeric.IsDigit: Checks if all characters in the input string are digits.Regex Replace: Performs a regex-based replacement of `param_1` with `param_2` in the input string.JSON Serialize: Converts the input string to a JSON formatted string.Regex: Finds all occurrences of the pattern `param_1` in the input string, joins them using `param_2` (defaulting to ", "), and returns the result.DecodeBase64: Decodes the input string from base64 using `param_1` as the encoding type. Default to utf-8EncodeBase64: Encodes the input string in base64 using `param_1` as the encoding type. Default to utf-8RemoveNewLines: Removes new lines from the input string, replacing them with spaces.Split: Splits the input string using `param_1` (or "," if not provided) and adds the result to the Siemplify result.|Functions|String Functions|
|NO_COMPUTE_INSTANCE_REMEDIATION_SUMMARY|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Init Remediation|The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|
|Count Ec2|Count the number of entities from a specific scope.|SiemplifyUtilities|Count Entities In Scope|
|COMPUTE_INSTANCE_REMEDIATION_SUMMARY |The action sets a key and value in a specific context (alert or case)|Tools|Set Context Value|

