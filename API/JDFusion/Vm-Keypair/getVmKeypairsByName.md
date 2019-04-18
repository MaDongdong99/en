# getVmKeypairsByName


## Description
Search Information of corresponding key pair resource according to the cloud provider

## Request Method
GET

## Request Address
https://jdfusion.jdcloud-api.com/v1/regions/{regionId}/vm_keypairs/{name}

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**name**|String|True| |keypair name|
|**regionId**|String|True| |Region ID|

## Request Parameter
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**x-jdcloud-nonce**|String|True| |See guide document of signature algorithm for obtaining method|
|**x-jdcloud-date**|String|True| |See guide document of signature algorithm for obtaining method|
|**authorization**|String|True| |See guide document of signature algorithm for obtaining method|
|**x-jdcloud-fusion-cloudid**|String|False| |Cloud Registration Information ID|


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result| |
|**requestId**|String|Request ID|

### Result
|Name|Type|Description|
|---|---|---|
|**keypair**|KeypairInfo| |
### KeypairInfo
|Name|Type|Description|
|---|---|---|
|**name**|String|Key Pair Name|
|**keyFingerprint**|String|Key Fingerprint|
|**cloudID**|String|Cloud Registration Information ID|

## Return Code
|Return Code|Description|
|---|---|
|**200**|ok|
|**404**|not found|
