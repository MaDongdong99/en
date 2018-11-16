# addUserViewIP


## Description
Add customized resolution ISP line of domain name

## Request Method
POST

## Request Address
https://clouddnsservice.jdcloud-api.com/v1/regions/{regionId}/userview/addUserViewIP

|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|

## Request Parameter
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**req**|AddViewIP|True| |Add parameters of customized resolution ISP line of domain name|

### AddViewIP
|Name|Type|Required or Not|Default Value|Description|
|---|---|---|---|---|
|**domainId**|Integer|False| |Domain Name ID|
|**ipRanges**|String[]|False| |This ISP line needs to add IP segment. <br><br> IP segment supports two formats of 1.2.3.4-5.6.7.8 and 1.2.3.4/16 <br>|
|**viewId**|Integer|False| |Customized ISP Line ID|
|**viewName**|String|False| |Customized ISP Line Name with 64 Characters at most|

## Return Parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String| |


## Return Code
|Return Code|Description|
|---|---|
|**200**|OK|
|**400**|BAD_REQUEST|
