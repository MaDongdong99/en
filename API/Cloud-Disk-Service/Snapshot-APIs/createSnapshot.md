# createSnapshot


## Description
-   Create a snapshot for the specified cloud disk, and the status of the newly generated snapshot is creating.
-   The quota for single-user snapshots in the same region is 15.
-   To ensure data integrity, please stop writing to the cloud disk before creating a snapshot to ensure the integrity of snapshot data.
-   Before creating a snapshot, we suggest you detach the cloud disk and reattach the disk to the virtual machine after the snapshot is created.
-   The life cycle of manual snapshots is independent from the cloud disk. Please delete unnecessary snapshots in time.
-   The time demanded to create a snapshot depends on the capacity of the cloud disk. The larger the capacity is, the longer it will take.


## Request method
POST

## Request address
https://disk.jdcloud-api.com/v1/regions/{regionId}/snapshots

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**snapshotSpec**|SnapshotSpec|True| |snapshot specification|
|**clientToken**|String|True| |Idempotence Check Parameter|

### SnapshotSpec
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**name**|String|True| |Snapshot Name|
|**description**|String|False| |Snapshot Description|
|**diskId**|String|True| |Cloud Disk ID used to create the Snapshot|

## Response parameter
|Name|Type|Description|
|---|---|---|
|**result**|Result|Result Set|
|**requestId**|String|Request ID|

### Result
|Name|Type|Description|
|---|---|---|
|**snapshotId**|String|ID of the Created Snapshot|

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
