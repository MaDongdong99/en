# Create Cloud Disk

JD Cloud & AI provides you with a variety of ways to create a cloud disk:

* Create a cloud disk when the instance is created. For details, please refer to [Create Instance](../Instance/Create-Instance.md);
* Separately [Create Cloud Disk](http://docs.jdcloud.com/en/cloud-disk-service/create-cloud-disk);
* [Create Disk from Snapshot](http://docs.jdcloud.com/en/cloud-disk-service/create-disk-by-snapshot), namely, you can keep historical time point data of a certain cloud disk in the new disk.


		Please note:
		* By default, the quota for cloud disks in each region is 15, and it can be increased by opening ticket;
        * A single instance can support attaching up to 8 cloud disks;
        * Each general SSD Cloud Disk, performance-oriented SSD Cloud Disk or capacity-oriented HDD Cloud Disk supports a maximum capacity of 4,000G; Each SSD cloud disk supports a maximum capacity of 1,000G; each Premium Hdd cloud disk supports a maximum capacity of 3,000G;
        * It supports specifying the cloud disk encryption attribute at the time of creating a null data disk, and the encryption attribute cannot be changed upon configuration and will be inherited to any snapshot created based on the disk; in a similar way, if a data disk is created from snapshot, the encryption attribute of the cloud disk depends on the snapshot;
        * If you need to create a cloud disk billed by configuration, you need to ensure that your balance plus available coupon is no less than RMB 50. Please recharge if the current balance is insufficient;
        * The current instance does not support merging of multiple cloud disks. After the creation, each cloud disk is an independent entity, and it is impossible to merge the spaces of multiple cloud disks by formatting. It is recommended that you plan the number and capacity of disks in advance; if the cloud disk has been created, but you need to expand it, you can follow these steps:
          * For cloud disk under monthly package, capacity expansion can be realized by expanding the cloud disk;
          * You can create a cloud disk snapshot for the cloud disk billed by configuration, and then create a new disk from snapshot. Then, the old disk can be deleted.

## Related Reference
[Create Instance](../Instance/Create-Instance.md)

[Create Cloud Disk](http://docs.jdcloud.com/en/cloud-disk-service/create-cloud-disk)


[Create A Cloud Disk from Snapshot](http://docs.jdcloud.com/en/cloud-disk-service/create-disk-by-snapshot)