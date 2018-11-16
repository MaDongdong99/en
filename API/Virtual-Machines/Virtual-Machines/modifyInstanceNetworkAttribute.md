# modifyInstanceNetworkAttribute


## Description
Modify the ENI attributes of the VM, including whether to delete ENI with the VM. 

The attributes of primary network interface cannot be modified.


## Request method
POST

## Request address
https://vm.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:modifyInstanceNetworkAttribute

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**instanceId**|String|True| |VM ID|
|**regionId**|String|True| |Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**networks**|InstanceNetworkAttribute[]|False| |List of ENIs|

### InstanceNetworkAttribute
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**autoDelete**|Boolean|False| |Auto-delete with the machine, False by default.|
|**networkInterfaceId**|String|False| |ENI ID|

## Response parameter
None


## Response code
|Return code|Description|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|

