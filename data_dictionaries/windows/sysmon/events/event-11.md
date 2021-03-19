# Event ID 11: FileCreate
###### Version: 4.32

## Description
**File create** operations are logged when a file is created or overwritten. This event is useful for monitoring autostart locations, like the Startup folder, as well as temporary and download directories, which are common places malware drops during initial infection.

## Data Dictionary
|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|tag|RuleName|string|custom tag mapped to event. i.e ATT&CK technique ID|`T1114`|
|event_creation_time|UtcTime|date|Time in UTC when event was created|`4/11/18 6:01`|
|process_guid|ProcessGuid|string|Process Guid of the process that created the file|`{A98268C1-958A-5ACD-0000-0010C62F0100}`|
|process_id|ProcessId|integer|Process ID used by the os to identify the process that created the file (child)|`1044`|
|process_file_path|Image|string|File path of the process that created the file|`C:\WINDOWS\System32\svchost.exe`|
|file_name|TargetFilename|string|Name of the file|`C:\Windows\Prefetch\CONHOST.EXE-1F3E9D7E.pf`|
|file_creation_time|CreationUtcTime|date|File creation time|`12/4/17 17:38`|

## References
* [Sysmon Source](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-11-filecreate)
* [TrustedSec Sysmon Community Guide](https://github.com/trustedsec/SysmonCommunityGuide/blob/master/file-create.md)
