# describeInstanceAttributes


## Description
Query the details of the RDS instance (MySQL, SQL Server, etc.) and the MySQL read-only instance details

## Request method
GET

## Request address
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region code, with range detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|
|**instanceId**|String|True| |RDS instance ID, which uniquely identifies an RDS instance|

## Request parameter
None


## Response parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result| |

### Result
|Name|Type|Description|
|---|---|---|
|**dbInstanceAttributes**|DBInstanceAttribute| |
### DBInstanceAttribute
|Name|Type|Description|
|---|---|---|
|**instanceId**|String|Instance ID|
|**instanceName**|String|Instance name with specific rules detailed in the Help Center Documentation: [Name and Password Restrictions](../../../documentation/Cloud-Database-and-Cache/RDS/Introduction/Restrictions/SQLServer-Restrictions.md)|
|**instanceType**|String|Instance type, such as primary instances, read-only instances, etc., detailed in [Enumeration Parameter Definition](../Enum-Definitions/Enum-Definitions.md)|
|**engine**|String|Instance engine type, such as MySQL or SQL Server, etc., detailed in [Enumeration Parameter Definition](../Enum-Definitions/Enum-Definitions.md)|
|**engineVersion**|String|Instance engine version, detailed in [Enumeration Parameter Definition](../Enum-Definitions/Enum-Definitions.md)|
|**instanceClass**|String|Instance Type Code|
|**instanceStorageGB**|Integer|Disk, Unit: GB|
|**instanceCPU**|Integer|Number of CPU Cores|
|**instanceMemoryMB**|Integer|Memory Size, Unit: MB|
|**regionId**|String|Region ID, detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|
|**azId**|String[]|AZ ID, the first is AZ for the primary instance, which is detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|
|**vpcId**|String|VPC ID|
|**subnetId**|String|Subnet ID|
|**internalDomainName**|String|Intranet Domain of Instance|
|**publicDomainName**|String|Internet Domain of Instance|
|**instancePort**|String|Application Access Port|
|**connectionMode**|String|Access  Mode, detailed in [Enumeration Parameter Definition](../Enum-Definitions/Enum-Definitions.md)|
|**auditStatus**|String|Audit status, detailed in [Enumeration Parameter Definition](../Enum-Definitions/Enum-Definitions.md)|
|**instanceStatus**|String|Instance status, detailed in [Enumeration Parameter Definition](../Enum-Definitions/Enum-Definitions.md)|
|**createTime**|String|Instance Creation Time|
|**charge**|Charge|Billing Configuration|
|**primaryNode**|DBInstanceNode|Information of master node in High Availability Cluster<br>- only support SQL Serverer|
|**secondaryNode**|DBInstanceNode|Information of slave node in High Availability Cluster<br>- only support SQL Serverer|
|**tags**|Tag[]|Tag Information|
### Tag
|Name|Type|Description|
|---|---|---|
|**key**|String|Tag Key|
|**value**|String|Tag Value|
### DBInstanceNode
|Name|Type|Description|
|---|---|---|
|**id**|String|Nodeid|
|**name**|String|Node Name|
|**status**|String|Node Status|
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
