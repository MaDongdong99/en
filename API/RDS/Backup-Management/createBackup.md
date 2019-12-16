# createBackup


## Description
Creating a full backup of the RDS instance can be fully backed up for the entire instance or part of the database (SQL Server supports only). At the same time, there is only be one running backup task can work<br>- Support SQL Server only

## Request method
POST

## Request address
https://rds.jdcloud-api.com/v1/regions/{regionId}/backups

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region code, with range detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**instanceId**|String|False| |RDS instance ID can identify an instance uniquely|
|**backupSpec**|[BackupSpec](createBackup#BackupSpec)|False| |Backup Specification|

### <a name="BackupSpec">BackupSpec</a>
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**backupName**|String|False| |Backup name with length up to 64 English characters or Chinese characters of equal length|
|**dbNames**|String[]|False| |List of Database Names to Be Backed up. If it is not filled, the whole instance will be backed up<br>- **MySQL: not support the parameter**<br>- **SQL Server: support**|

## Response parameter
|Name|Type|Description|
|---|---|---|
|**result**|[Result](createBackup#Result)| |

### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**backupId**|String|Backup Id|

## Response code
|Return code|Description|
|---|---|
|**200**|OK|
