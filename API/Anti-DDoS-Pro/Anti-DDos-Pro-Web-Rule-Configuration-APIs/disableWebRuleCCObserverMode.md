# disableWebRuleCCObserverMode


## Description
Disable CC observer mode of web service rules, CC defense only alarms and does not defense in observe mode. Support batch operations, multiple webRuleId, separated by ',', can be uploaded in batch operations, when result.code returns 1, representing operation succeeded, when 0, representing all or part of the operations may fail

## Request Method
POST

## Request Address
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/webRules/{webRuleId}:disableCCObserverMode

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID, Anti-DDoS Pro dose not differentiate regions, upload to cn-north-1 directly|
|**instanceId**|String|True| |Anti-DDoS Pro instance Id|
|**webRuleId**|String|True| |Web Rule Id|

## Request Parameter
None


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result| |
|**requestId**|String| |
|**error**|Error| |

### Error
|Name|Type|Description|
|---|---|---|
|**err**|Err| |
### Err
|Name|Type|Description|
|---|---|---|
|**code**|Long|Same as http code|
|**details**|Object| |
|**message**|String| |
|**status**|String|Specific Error|
### Result
|Name|Type|Description|
|---|---|---|
|**code**|Integer|0: Disabling CC observer mode failed, 1: Disabling CC observer mode succeeded|
|**message**|String|Specify reasons when disabling CC observer mode failed|

## Return Code
|Return Code|Description|
|---|---|
|**200**|OK|
