# Core Concepts

|English|Chinese|Description|
| - | - | - |
|Bucket|Bucket|Bucket is the fundamental organization unit of data in Object Storage Service and all data must be a Bucket. The name of Bucket is globally unique, global refers to the regions supported by OSS. If you create a Bucket of a certain name, then other users cannot create a Bucket with the same name|
|Object|Object or file|Object is the fundamental entity in JD Object Storage Service. In this help documentation, Object, Object and File represent the same meaning; object is composed of Key, Data and Metadata|
|Endpoint|OSS access domain|Object Storage Service allocates an Internet access domain and an intranet access domain for each Bucket by default|
|Region|Region or data center|Region where storage cluster locates, currently supports four data centers: cn-north-1, cn-south-1, cn-east-1, and cn-east-2|
|Accesskey|Joint name of AccessKeyId and AccessKeySecret|AccessKeyId and AccessKeySecret are the identity for user to access JD Object Storage Service. Users can log in user center to create AccessKeyId and AccessKeySecret after applying for and turning on use qualification for JD Cloud products|
|Put Object|Simple upload|User can upload a single Object by way of Put Object in APIs, which is applicable to the scenario where uploading can be done upon any HTTP request interaction, e.g. small file uploading|
|Multipart Upload|Multipart upload|Besides PUT Object, OSS provides another uploading mode --- Multipart Upload. If the user cannot determine the size of uploading file or the uploading file is large and requires breakpoint upload, use Multipart Upload uploading mode|
|Get Object|Download|Used to obatin a single Object|
|Object Meta|File metadata|A group of Key-Value combination, consisting of System-Defined Metadata and User-Defined Metadata. Metadata used to describe file information, e.g. length, type, etc.|
|Data|File data|Any type of data uploaded by user, such as text, multimedia, binary|
|Key|File name|Unique name identifier of Object, e.g. test.jpg|

