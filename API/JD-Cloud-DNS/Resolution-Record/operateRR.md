# operateRR


## Description
Enable, disable, or delete the resolution records under the main domain name

## Request method
POST

## Request address
https://clouddnsservice.jdcloud-api.com/v1/regions/{regionId}/domain/{domainId}/RROperate

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**domainId**|String|True| |Domain Name ID, please get it by using getDomains interface.|
|**regionId**|String|True| |Region ID to which the instance belongs|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**action**|String|True| |Operation Type, On->Enable, Off->Disable, Del->Delete|
|**ids**|Integer[]|True| |Resolution Record ID of the Operation Required|


## Response parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|ID of This Request|


## Response code
|Return code|Description|
|---|---|
|**200**|OK|
|**400**|BAD_REQUEST|
