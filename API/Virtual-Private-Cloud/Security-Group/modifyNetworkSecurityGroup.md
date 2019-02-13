# modifyNetworkSecurityGroup


## Description
Modify security group attribute

## Request method
PATCH

## Request address
https://vpc.jdcloud-api.com/v1/regions/{regionId}/networkSecurityGroups/{networkSecurityGroupId}

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|
|**networkSecurityGroupId**|String|True| |NetworkSecurityGroup ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**networkSecurityGroupName**|String|False| |Security Group Name. Value Range of Name: 1-32 Chinese, English capital and lowercase letters, numbers and underline delimiter|
|**description**|String|False| |Security Group Description. Value Range: 0-256 of all characters entered under UTF-8 coding|


## Response parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|Request ID|


## Response code
|Return code|Description|
|---|---|
|**200**|OK|
|**400**|Request parameter x.y.z is 'xxx', expected one of [yyy,zzz]|
|**404**|Resource not found|
