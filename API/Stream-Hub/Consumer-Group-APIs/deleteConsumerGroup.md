# deleteConsumerGroup


## Description
Delete ConsumerGroupName

## Request method
DELETE

## Request address
https://streambus.jdcloud-api.com/v1/regions/{regionId}/consumerGroup

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**consumerGroupId**|Integer|True| |Consumer Group ID|
|**topicId**|Integer|True| |Subject ID|


## Response parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String| |
|**result**|Result| |


### Result
|Name|Type|Description|
|---|---|---|
|**message**|String| |
|**status**|Boolean| |

## Response code
|Return code|Description|
|---|---|
|**200**|OK|
|**401**|STREAMHUB_UNAUTHENTICATED|
|**400**|UNAUTHENTICATED|
