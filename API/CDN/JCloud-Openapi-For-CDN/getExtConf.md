# getExtConf


## Description
Rare Configuration for Live Streaming Domain Search

## Request Method
GET

## Request Address
https://cdn.jdcloud-api.com/v1/liveDomain/{domain}/extConf:query

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**domain**|String|True| |User Domain|

## Request Parameter
None


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**result**|[Result](#result)| |
|**requestId**|String| |

### <div id="Result">Result</div>
|Name|Type|Description|
|---|---|---|
|**data**|String| |

## Return Code
|Return Code|Description|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|
