# createSecret


## Description
Create a secret for storing relevant confidential information of image registry.


## Request method
POST

## Request address
https://nativecontainer.jdcloud-api.com/v1/regions/{regionId}/secrets

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**name**|String|True| |Names of confidential data can’t be the same<br>|
|**secretType**|String|True| |Now, only the following confidential data type is supported: docker-registry, which is the docker registry verification type.<br>|
|**data**|DockerRegistryData|False| |Confidential data. <br><br>Valid characters of key include letters, numbers, -, _ and .; <br><br>The value is the character string encoded by Base64, which can’t comprise a line break (please use base64 -w 0 option under linux); the length cap of each value is 4KB; and the length of the entire data can’t exceed 256KB; <br><br>Fields as server, username and password must be contained and the field of email is optional. <br><br>|

### DockerRegistryData
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**server**|String|True| |Registry Server Address|
|**username**|String|True| |User Name|
|**password**|String|True| |Password |
|**email**|String|False| |Email Address|

## Response parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result| |
|**requestId**|String| |

### Result
|Name|Type|Description|
|---|---|---|
|**secretName**|String| |

## Response code
|Return code|Description|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**429**|Quota exceeded|
|**500**|Internal server error|
|**503**|Service unavailable|
