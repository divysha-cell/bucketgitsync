
# VSphere

VMware vSphere is a VMware cloud computing platform for virtualization.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|IP_OR_HOST|x.x.x.x|
|Username||True|String||
|Password||True|Password|*****|
|Port||True|Int|443|


#### Dependencies
| |
|-|
|pyvmomi-9.0.0.0-py3-none-any.whl|


## Actions
#### List Vms
Get a list of all registered VMs
Timeout - 600 Seconds



##### JSON Results
```json
[{"Guest": "Microsoft Windows 7 (64-bit)", "Bios UUID": "423503ea-af3c-58a8-188c-f6285cec98e5", "VMware Tools": "toolsNotInstalled", "Ip Address": "1.1.1.1", "State": "poweredOn", "Template": false, "Path": "[DataStore] vm/vn.vmx", "Name": "vm", "Instance UUID": "50359be7-424b-e53d-5133-3f98f0e705ef"}]
```



#### Get System Info
Get information about a VM
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|Target VM name.|True|String||



##### JSON Results
```json
{"Guest": "Microsoft Windows 7 (64-bit)", "Bios UUID": "423503ea-af3c-58a8-188c-f6285cec98e5", "VMware Tools": "toolsNotInstalled", "Ip Address": "1.1.1.1", "State": "poweredOn", "Template": false, "Path": "[DataStore] vm/vn.vmx", "Name": "vm", "Instance UUID": "50359be7-424b-e53d-5133-3f98f0e705ef"}
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Power Off
Power off a VM
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|Target VM name.|True|String||



#### Power On
Power on a VM
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|Vm Name|True|String|Target VM name.|



#### Reset
Hard reset a VM
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|The name of the target VM.|True|String||



#### Get Vm By Ip
Get VM name by IP address
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"Guest": "Microsoft Windows 7 (64-bit)", "Bios UUID": "423503ea-af3c-58a8-188c-f6285cec98e5", "VMware Tools": "toolsNotInstalled", "Ip Address": "1.1.1.1", "State": "poweredOn", "Template": false, "Path": "[DataStore] vm/vn.vmx", "Instance UUID": "50359be7-424b-e53d-5133-3f98f0e705ef", "Name": "vm"}, "Entity": "1.1.1.1"}]
```



#### Suspend
Suspend a VM
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|The name of the target VM.|True|String||



#### Take Snapshot
Take a snapshot of a VM
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|The name of the target VM.|True|String||
|Snapshot Name|The name of the target snapshot.|True|String||
|Snapshot Description|Snapshot description value.|True|String||



#### Revert To Snapshot
Revert to a specific snapshot
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm Name|The name of the target VM.|True|String||
|Snapshot Name|The name of the target snapshot.|True|String||









