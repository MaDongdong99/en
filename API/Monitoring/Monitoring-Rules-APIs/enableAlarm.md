# enableAlarm


## Description
Enable the alarm rule, when the alarm rule is in the status of “Disabled”, the alarm rule can be enabled by using the API.

## Request method
POST

## Request address
https://monitor.jcloud.com/v1/regions/{regionId}/alarms/{alarmId}:enable

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**alarmId**|String|True| |Rule ID|
|**regionId**|String|True| |Region ID|

## Request parameter
None


## Response parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|Request ID|


## Response code
|Return code|Description|
|---|---|
|**200**|OK|
