# describeErrorLogs


## Description
Obtain error logs of SQL Server and download information<br>- only support SQL Server

## Request method
GET

## Request address
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/errorLogs

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**instanceId**|String|True| |RDS instance ID, which uniquely identifies an RDS instance|
|**regionId**|String|True| |Region code, with range detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|

## Request parameter
None


## Response parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result| |


### Result
|Name|Type|Description|
|---|---|---|
|**errorLogs**|ErrorLog[]|Collection of Error Log Files|
### ErrorLog
|Name|Type|Description|
|---|---|---|
|**internalURL**|String|Download Link of Intranet|
|**lastUpdateTime**|String|Last Update Time of the Error Log, Format: YYYY-MM-DD HH:mm:ss|
|**name**|String|Error Log File Name|
|**publicURL**|String|Download Link of Public Network|
|**sizeByte**|Integer|Error Log File Size in Bytes|
|**uploadTime**|String|Error Log Upload Time, Format: YYYY-MM-DD HH:mm:ss|

## Response code
|Return code|Description|
|---|---|
|**200**|OK|
