# describeSecret


## Description
Search details of a single secrete


## Request method
GET

## Request address
https://nc.jdcloud-api.com/v1/regions/{regionId}/secrets/{name}

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**name**|String|True| |Secret Name|
|**regionId**|String|True| |Region ID|

## Request parameter
None


## Response parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String| |
|**result**|Result| |


### Result
|Name|Type|Description|
|---|---|---|
|**secret**|Secret| |
### Secret
|Name|Type|Description|
|---|---|---|
|**createdAt**|String|Creation Time|
|**data**|DockerRegistryData|Confidential Data|
|**name**|String|Confidential Data Name|
|**type**|String|Now, only the following private data type is supported: docker-registry, which is the docker registry verification type.|
### DockerRegistryData
|Name|Type|Description|
|---|---|---|
|**email**|String|Email Address|
|**password**|String|Password |
|**server**|String|Registry Server Address|
|**username**|String|User Name|

## Response code
|Return code|Description|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
