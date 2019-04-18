# deleteVpcSecurityGroupById


## Description
Delete Security Group

## Request Method
DELETE

## Request Address
https://jdfusion.jdcloud-api.com/v1/regions/{regionId}/vpc_securityGroups/{id}

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**id**|String|True| |SecurityGroup ID|
|**regionId**|String|True| |Region ID|

## Request Parameter
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**x-jdcloud-nonce**|String|True| |See guide document of signature algorithm for obtaining method|
|**x-jdcloud-date**|String|True| |See guide document of signature algorithm for obtaining method|
|**authorization**|String|True| |See guide document of signature algorithm for obtaining method|
|**x-jdcloud-fusion-cloudid**|String|True| |Cloud Registration Information ID|


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|Request ID|


## Return Code
|Return Code|Description|
|---|---|
|**204**|OK|
|**404**|securityGroup not found|
