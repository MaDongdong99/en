# Use constraint



- Cloud Disk Service must be attached to theVirtual Machines under the same region or the same availability zone
- In case of creating a new disk based on snapshot, the minimum selectable capacity of the new Cloud Disk Service is same as the snapshot capacity, and the maximum capacity is limited by the disk type
- Cloud Disk Service must be in available status when upgrading the capacity or recovering data based on snapshot

## The following table is the constraint on using Cloud Disk Service:


| Resource	| Quota	| Exceptional application method |
| :- | :- | :- |
|Number of Cloud Disk Services under a single account	|40 blocks under the same region|Ticket|
|Number of Cloud Disk Services attachable to a single machine	|8 blocks under the same region	|Unmodifiable|
|Number of snapshots under a single account	|15 blocks under the same region|Unmodifiable|



