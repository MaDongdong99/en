# describeElasticIps


## Description
Query Elastic IP List

## Request method
GET

## Request address
https://vpc.jdcloud-api.com/v1/regions/{regionId}/elasticIps/

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**pageNumber**|Integer|False|1|Page; it is 1 by default. Value Range: [1,∞); when the pages exceed total pages, show the last page|
|**pageSize**|Integer|False|20|Paging Size: 20 by default. Value Range: [10, 100]|
|**filters**|Filter[]|False| |elasticIpIds - ElasticIP ID Array Conditions, Support Multiple IDs<br>elasticIpAddress - EIP IP Address, Support Single Address<br>chargeStatus	- EIP Payment Status, Normal (normal status) or Overdue (Pay-In-Advance expired) or Arrear(arrear status), Support Single Status<br>|

### Filter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**name**|String|True| |Name of Filter Requirements|
|**operator**|String|False| |Operator of filter requirements is eq by default|
|**values**|String[]|True| |Value of Filter Requirements|

## Response parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result|Returned Results|
|**requestId**|String|Request ID|

### Result
|Name|Type|Description|
|---|---|---|
|**elasticIps**|ElasticIp[]|ElasticIp Resource Information List|
|**totalCount**|Integer|Total Number|
### ElasticIp
|Name|Type|Description|
|---|---|---|
|**elasticIpId**|String|Elastic IP ID|
|**elasticIpAddress**|String|Elastic IP Address|
|**bandwidthMbps**|Integer|Elastic IP Speed Limit (unit: Mbps)|
|**provider**|String|IP Service Provider, Values include bgp or no_bgp|
|**privateIpAddress**|String|IPV4 Address of Private IP|
|**networkInterfaceId**|String|Configure Elastic Network Interface ID|
|**instanceId**|String|Instance ID|
|**instanceType**|String|Instance Type|
|**charge**|Charge|Billing Configuration|
|**createdTime**|String|Creation Time of Elastic IP|
|**az**|String|If the availability zone of elastic ip is null, it means that all availability zones are available.|
### Charge
|Name|Type|Description|
|---|---|---|
|**chargeMode**|String|Payment Model, the value shall be prepaid_by_duration, postpaid_by_usage or postpaid_by_duration; prepaid_by_duration refers to Pay-In-Advance; postpaid_by_usage refers to Pay By Consumption and Pay-As-You-Go; postpaid_by_duration refers to Pay By Configuration and Pay-As-You-Go, and is postpaid_by_duration by default|
|**chargeStatus**|String|Cost Payment Status, the value is respectively normal, overdue and arrear.|
|**chargeStartTime**|String|The start time of the billing shall be subject to ISO8601, with the UTC time used in the format of YYYY-MM-DDTHH:mm:ssZ|
|**chargeExpiredTime**|String|Expiration Time, i.e. the expiration time of Pay-In-Advance resource, which shall be subject to ISO8601, with the UTC time used in the format of YYYY-MM-DDTHH:mm:ssZ. Pay-As-You-Go resource field is blank.|
|**chargeRetireTime**|String|The Expected Release Time refers to the expected release time of resources. This value is both available for the Pay-In-Advance/Pay-As-You-Go resources, conforming to the ISO8601 standard, with the UTC time used in the format of YYYY-MM-DDTHH:mm:ssZ|

## Response code
|Return code|Description|
|---|---|
|**200**|OK|
|**400**|invalid parameter|
|**401**|Authentication failed|
