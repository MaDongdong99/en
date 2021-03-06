# deleteDomain


## Description
Delete domain. Before carrying out the operation, please confirm such domain is out of service.

## Request Method
DELETE

## Request Address
https://vod.jdcloud-api.com/v1/domains/{domainId}

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**domainId**|Long|True| |Domain Name ID|

## Request Parameter
None


## Return Parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|Request ID|


## Return Code
|Return Code|Description|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|

## Request Example
DELETE
```
https://vod.jdcloud-api.com/v1/domains/2

```

