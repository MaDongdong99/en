# createRdsAccounts


## Description
Create an account with designated RDS instance according to provided information

## Request Method
POST

## Request Address
https://jdfusion.jdcloud-api.com/v1/regions/{regionId}/rds_instances/{instId}/accounts

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**instId**|String|True| |RDS Instance ID|
|**regionId**|String|True| |Region ID|

## Request Parameter
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**x-jdcloud-fusion-cloudid**|String|True| |Cloud Registration Information ID|
|**account**|CreateRDSAccount|True| |Create account information of RDS instance|

### CreateRDSAccount
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**name**|String|True| |Account Name|
|**password**|String|True| |Password|

## Return Parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result| |
|**requestId**|String|Request ID|

### Result
|Name|Type|Description|
|---|---|---|
|**task**|ResourceTFInfo| |
### ResourceTFInfo
|Name|Type|Description|
|---|---|---|
|**uuid**|String|uuid|
|**body**|String|Request Body|
|**status**|String|Status|
|**result**|String|Execution Results|
|**createdTime**|String|Creation Time|
|**updateTime**|String|Update Time|
|**provider**|String|cloud provider|
|**cloudId**|String|cloud ID|
|**userId**|String|user ID|

## Return Code
|Return Code|Description|
|---|---|
|**202**|ACCEPTED|
|**404**|RDS instance not found|
