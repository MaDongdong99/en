# Specifications

The JCS for MongoDB currently supports the following instance specifications.

## Replica Set Instance Type

### SSD Storage Type of Local Disk

| Specification Code | Specifications | Maximum Connection Number | Maximum IOPS | Storage Space |
| :--------------- | :------- | :--------- | :------- | :-------- |
| mongo.s1.small   | 1 Core 2G   | 500        | 1000     | 10G-1000G |
| mongo.s1.medium  | 2 Core 4G   | 1000       | 2000     | 10G-1000G |
| mongo.s1.large   | 4 Core 8G   | 2000       | 4000     | 10G-2000G |
| mongo.s1.xlarge  | 8 Core 16G  | 4000       | 8000     | 10G-2000G |
| mongo.s2.2xlarge | 8 Core 32G  | 8000       | 14000    | 10G-3000G |
| mongo.s2.4xlarge | 16 Core 64G | 16000      | 16000    | 10G-3000G |
| mongo.s2.8xlarge | 32 Core 128G | 32000      | 20000    | 10G-3000G |

### SSD Cloud Disk Storage Type

| Specification Code         | Specification    | Maximum Connections | Maximum IOPS               | Bucket  |
| :--------------- | :------- | :--------- | :--------------------- | :-------- |
| mongo.s1.small   | 1 Core 2G   | 500        | min{ 50 * Capacity, 32000} | 10G-1000G |
| mongo.s1.medium  | 2 Core 4G   | 1000       | min{ 50 * Capacity, 32000} | 10G-1000G |
| mongo.s1.large   | 4 Core 8G   | 2000       | min{ 50 * Capacity, 32000} | 10G-2000G |
| mongo.s1.xlarge  | 8 Core 16G  | 4000       | min{ 50 * Capacity, 32000} | 10G-2000G |
| mongo.s2.2xlarge | 8 Core 32G  | 8000       | min{ 50 * Capacity, 32000} | 10G-3000G |
| mongo.s2.4xlarge | 16 Core 64G | 16000      | min{ 50 * Capacity, 32000} | 10G-3000G |
| mongo.s2.8xlarge | 32 Core 128G | 32000      | min{ 50 * Capacity, 32000} | 10G-3000G |

## Sharded Cluster Instance Type

### SSD Storage Type of Local Disk

#### mongos

| Specification Code | Specification | Maximum Connections |
| :---------------- | :------- | :--------- |
| mongos.m1.small   | 1 Core 2G   | 1000       |
| mongos.m1.medium  | 2 Core 4G   | 2000       |
| mongos.m1.large   | 4 Core 8G   | 4000       |
| mongos.m1.xlarge  | 8 Core 16G  | 8000       |
| mongos.m1.2xlarge | 8 Core 32G  | 16000      |
| mongos.m1.4xlarge | 16 Core 64G | 32000      |
| mongos.m1.8xlarge | 32 Core 128G | 64000      |

#### configserver

| Specification Code       | Specification  | Maximum Connections | Maximum IOPS | Bucket |
| :------------- | :---- | :--------- | :------- | :------- |
| mongo.m1.small | 1 Core 2G | 500        | 1000     | 20G      |

#### shard

| Specification Code | Specification | Maximum Connections | Maximum IOPS |
| :--------------- | :------- | :--------- | :------- | --------- |
| mongo.m1.small   | 1 Core 2G   | 500        | 1000     | 10G-1000G |
| mongo.m1.medium  | 2 Core 4G   | 1000       | 2000     | 10G-1000G |
| mongo.m1.large   | 4 Core 8G   | 2000       | 4000     | 10G-2000G |
| mongo.m1.xlarge  | 8 Core 16G  | 4000       | 8000     | 10G-2000G |
| mongo.m1.2xlarge | 8 Core 32G  | 8000       | 14000    | 10G-3000G |
| mongo.m1.4xlarge | 16 Core 64G | 16000       | 16000    | 10G-3000G |
| mongo.m1.8xlarge | 32 Core 128G | 32000      | 20000    | 10G-3000G |

### SSD Cloud Disk Storage Type

#### mongos

| Specification Code          | Specification     | Maximum Connections |
| :---------------- | :------- | :--------- |
| mongos.m1.small   | 1 Core 2G    | 1000       |
| mongos.m1.medium  | 2 Core 4G    | 2000       |
| mongos.m1.large   | 4 Core 8G    | 4000       |
| mongos.m1.xlarge  | 8 Core 16G   | 8000       |
| mongos.m1.2xlarge | 8 Core 32G   | 16000      |
| mongos.m1.4xlarge | 16 Core 64G  | 32000      |
| mongos.m1.8xlarge | 32 Core 128G | 64000      |

#### configserver

| Specification Code       | Specification  | Maximum Connections | Maximum IOPS | Bucket |
| :------------- | :---- | :--------- | :------- | :------- |
| mongo.m1.small | 1 Core 2G | 500        | 1000     | 20G      |

#### shard

| Specification Code         | Specification     | Maximum Connections | Maximum IOPS               | Bucket  |
| :--------------- | :------- | :--------- | :--------------------- | --------- |
| mongo.m1.small   | 1 Core 2G    | 500        | min{ 50 * capacity, 32000} | 10G-1000G |
| mongo.m1.medium  | 2 Core 4G    | 1000       | min{ 50 * capacity, 32000} | 10G-1000G |
| mongo.m1.large   | 4 Core 8G    | 2000       | min{ 50 * capacity, 32000} | 10G-2000G |
| mongo.m1.xlarge  | 8 Core 16G   | 4000       | min{ 50 * capacity, 32000} | 10G-2000G |
| mongo.m1.2xlarge | 8 Core 32G   | 8000       | min{ 50 * capacity, 32000} | 10G-3000G |
| mongo.m1.4xlarge | 16 Core 64G  | 16000      | min{ 50 * capacity, 32000} | 10G-3000G |
| mongo.m1.8xlarge | 32 Core 128G | 32000      | min{ 50 * capacity, 32000} | 10G-3000G |

## Related References


- [Price Overview](../Pricing/Price-Overview.md)
- [Billing Rules](../Pricing/Billing-Rules.md)
- [Create Instance](../Getting-Started/Create-Instance.md)
