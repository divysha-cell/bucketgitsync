
# WMI

Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.

Python Version - 3



## Actions
#### ListUsers
List all users configured on a system
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|Server Address|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|



##### JSON Results
```json
[{"Status": "Degraded", "Domain": "PC-01", "Description": "Built-in account for administering the computer/domain", "InstallDate": null, "Caption": "PC-01\\Administrator", "Disabled": true, "PasswordChangeable": true, "Lockout": false, "AccountType": 512, "SID": "S-1-5-21-3501119061-1410835827-1917537121-500", "LocalAccount": true, "FullName": "", "SIDType": 1, "PasswordRequired": true, "PasswordExpires": false, "Name": "Administrator"}]
```



#### ListServices
Get the list of installed services on the system
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|Server Address|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|



##### JSON Results
```json
[{"DisplayName": "Adobe Flash Player Update Service", "ServiceSpecificExitCode": 0, "State": "Stopped", "SystemName": "PC-01", "ErrorControl": "Normal", "Status": "OK", "ProcessId": 0, "DesktopInteract": false, "Started": false, "AcceptStop": false, "CheckPoint": 0, "PathName": "C:\\Windows\\SysWOW64\\Macromed\\Flash\\FlashPlayerUpdateService.exe", "WaitHint": 0, "Name": "AdobeFlashPlayerUpdateSvc", "InstallDate": null, "Caption": "Adobe Flash Player Update Service", "StartMode": "Manual", "Description": "This service keeps your Adobe Flash Player installation up to date with the latest enhancements and security fixes.", "ServiceType": "Own Process", "TagId": 0, "DelayedAutoStart": false, "StartName": "LocalSystem", "AcceptPause": false, "CreationClassName": "Win32_Service", "SystemCreationClassName": "Win32_ComputerSystem", "ExitCode": 0}]
```



#### GetSystemInfo
Get information about a system
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|Server Address|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|



##### JSON Results
```json
{"NumberOfProcessors": 1, "MaxProcessMemorySize": "137438953344", "SystemDrive": "C:", "WakeUpType": 6, "ChassisSKUNumber": "Notebook", "BootROMSupported": true, "ForegroundApplicationBoost": 2, "OperatingSystemSKU": 126, "AdminPasswordStatus": 3, "SuiteMask": 272, "InstallDate": "20161205114436.000000+120", "Distributed": false, "EncryptionLevel": 256, "FrontPanelResetStatus": 3, "Debug": false, "Organization": "", "AutomaticManagedPagefile": true, "PowerSupplyState": 3, "InfraredSupported": false, "LargeSystemCache": null, "CodeSet": "1252", "FreeSpaceInPagingFiles": "2415000", "DataExecutionPrevention_32BitApplications": true, "PrimaryOwnerContact": null, "KeyboardPasswordStatus": 3, "BootStatus": [0, 0, 0], "MaxNumberOfProcesses": -1, "FreePhysicalMemory": "8962948", "DataExecutionPrevention_Available": true, "PCSystemTypeEx": 2, "CSDVersion": null, "PartOfDomain": true, "SystemFamily": "Latitude", "DomainRole": 1, "CurrentTimeZone": 120, "OSType": 18, "SystemDirectory": "C:\\Windows\\system32", "Workgroup": null, "CountryCode": "1", "NameFormat": null, "PAEEnabled": null, "AutomaticResetCapability": true, "DataExecutionPrevention_Drivers": true, "TotalVirtualMemorySize": "18896472", "NumberOfLicensedUsers": 0, "DataExecutionPrevention_SupportPolicy": 2, "TotalSwapSpaceSize": null, "PowerOnPasswordStatus": 3, "HypervisorPresent": false, "SystemStartupSetting": null, "LocalDateTime": "20180220173653.403000+120", "SystemDevice": "\\Device\\HarddiskVolume2", "PortableOperatingSystem": false, "Domain": "DOMAIN.COM", "TotalPhysicalMemory": "16799850496", "ChassisBootupState": 3, "SystemType": "x64-based PC", "DNSHostName": "PC-01", "EnableDaylightSavingsTime": true, "PCSystemType": 2, "PrimaryOwnerName": "Windows User", "WindowsDirectory": "C:\\Windows", "PowerState": 0, "ResetCount": -1, "LastLoadInfo": null, "ServicePackMinorVersion": 0, "OEMStringArray": ["Dell System", "1[07A0]", "3[1.0]"], "BootOptionOnWatchDog": null, "Status": "OK", "OSArchitecture": "64-bit", "SystemStartupOptions": null, "OSLanguage": 1033, "InitialLoadInfo": null, "Manufacturer": "Microsoft Corporation", "BuildType": "Multiprocessor Free", "FreeVirtualMemory": "9128168", "OtherTypeDescription": null, "OEMLogoBitmap": null, "ServicePackMajorVersion": 0, "Version": "10.0.14393", "ThermalState": 3, "LastBootUpTime": "20180218183758.487061+120", "SizeStoredInPagingFiles": "2490368", "NumberOfProcesses": 133, "PowerManagementSupported": null, "CSName": "PC-01", "SerialNumber": "00378-30000-00003-AA585", "MUILanguages": ["en-US"], "SupportContactDescription": null, "Primary": true, "SystemStartupDelay": null, "ResetLimit": -1, "ProductType": 1, "RegisteredUser": "Windows User", "Roles": ["LM_Workstation", "LM_Server", "SQLServer"], "PlusProductID": null, "ResetCapability": 1, "SystemSKUNumber": "07A0", "OSProductSuite": 256, "PauseAfterReset": "-1", "NumberOfUsers": 6, "BootupState": "Normal boot", "Name": "Microsoft Windows 10 Enterprise N 2016 LTSB|C:\\Windows|\\Device\\Harddisk0\\Partition2", "AutomaticResetBootOption": true, "Caption": "Microsoft Windows 10 Enterprise N 2016 LTSB", "TotalVisibleMemorySize": "16406104", "PowerManagementCapabilities": null, "Model": "Latitude 7480", "PlusVersionNumber": null, "Description": "", "NetworkServerModeEnabled": true, "NumberOfLogicalProcessors": 4, "BootOptionOnLimit": null, "Locale": "0409", "CSCreationClassName": "Win32_ComputerSystem", "UserName": "DOMAIN\\User", "BuildNumber": "14393", "DaylightInEffect": false, "CreationClassName": "Win32_OperatingSystem", "BootDevice": "\\Device\\HarddiskVolume1"}
```



#### RunQuery
Run an arbitary query using WQL on the system
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|Server Address|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|
|WQL Query|Query content(e.g: SELECT Caption, Description FROM Win32_LogicalDisk WHERE DriveType <> 3).|True|String||



##### JSON Results
```json
[{"Caption": "C:", "Description": "Local Fixed Disk", "DeviceID": "C:"}, {"Caption": "I:", "Description": "Local Fixed Disk", "DeviceID": "I:"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









