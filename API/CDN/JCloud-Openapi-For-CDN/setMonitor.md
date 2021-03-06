# setMonitor


## Description
Set monitoring information of origin server

## Request Method
POST

## Request Address
https://cdn.jdcloud-api.com/v1/domain/{domain}/monitor

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**domain**|String|True| |User Domain|

## Request Parameter
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**cycle**|Integer|True| |Detection period, value: 1 and 5, unit: minute|
|**monitorPath**|String|True| |Detection Path|
|**httpRequestHeader**|Object|False| |http Request Head|


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**result**|[Result](setmonitor#result)| |
|**requestId**|String| |

### <div id="result">Result</div>
|Name|Type|Description|
|---|---|---|
|**monitorId**|Long| |

## Return Code
|Return Code|Description|
|---|---|
|**200**|OK|
|**404**|NOT_FOUND|