# Put Object-Copy

## Description
Create the copy of an existed Object, the copy operation is equal to executing GET operation first and executing PUT operation next. Specify source Bucket and source Object to be replicated by x-amz-copy-source Header. In OSS, the maximum single Object that can be operated is 5G. In case of exceeding 5G, please use multipart upload of Upload Part-Copy operation. In order to execute the operation, you need READ permission of the source Bucket and WRITE permission of the Target Bucket.

When OSS receives Put Object-Copy request or it is executing Copy, the request may return an error. If the error occurred before executing Copy, you will receive an standard OSS error; if the error occurred during the Copy, the error of Copy will be embedded into 200 OK response, so Copy of 200 OK response result may be both successful or failed.

## Request
### Syntax
```
PUT /destinationObject HTTP/1.1
Host: <destinationBucket>.s3.<region>.jdcloud-oss.com 
x-amz-copy-source: /source_bucket/sourceObject
Authorization: <authorization string> (see Authenticating Requests (AWS Signature Version4))
Date: <date>
```
### Request Parameter
No Request Parameters
### Request Header
Except public request Headers, the following Headers also can be used

Name|Description|Must
---|---|---
x-amz-copy-source|Source Bucket and source Object name are separated by "/". <br>Type: String<br>Default: None<br>The character string must use URL encoding|Yes
x-amz-storage-class|If there is no specified header, the default storage type is Standard storage. <br>Type: Enum<br>Default: STANDARD<br>Valid Values: STANDARD, GLACIER, REDUCED_REDUNDANCY, STANDARD_IA|No
x-amz-metadata-directive|If the header value is specified as COPY, the metadata of the original file other than x-amz-storage-class will be replicated to the target file. The customized metadata specified by PutObjectCopy will be ignored at this time. <br> If it is specified as REPLACE, the metadata of the target file depends on the specified metadata requested by PutObjectCopy. <br>Type: String<br>Default: COPY<br>Valid values: COPY, REPLACE|No
x-amz-meta-\*|Header beginning with x-amz-meta-prefix is user-customized Header. The size of the customized Header (including key and value) cannot exceed 2K in UTF-8 encoding. |No

### Request Elements
No Request Elements

## Response
### Response Header
Except public response Headers, the operation can also use the following Headers

Name|Description
---|---
x-amz-storage-class|Provide storage type information of Object. In the case of non-standard storage, OSS will return the Header

### Response Element

Name|Description
---|---
CopyObjectResult|Response Element Information Set. <br>Type: Container<br>Ancestor: None
ETag|Return ETag of new Object. <br>Type: String<br>Ancestor: CopyObjectResult
LastModified|Return last modification time of the object. <br>Type: String<br>Ancestor: CopyObjectResult

## Examples
### Request Example
```
PUT /my-second-image.jpg HTTP/1.1
Host: oss-example.s3.<region>.jdcloud-oss.com
Date: Wed, 28 Oct 2009 22:32:00 GMT
x-amz-copy-source: /bucket/my-image.jpg
Authorization: <authorization string>
```

### Response Example
```
HTTP/1.1 200 OK
x-amz-request-id: 318BC8BC148832E5
Date: Wed, 28 Oct 2009 22:32:00 GMT
Connection: close
Server: JDCloudOSS

<CopyObjectResult>
   <LastModified>2009-10-28T22:32:00</LastModified>
   <ETag>"9b2cf535f27731c974343645a3985328"</ETag>
</CopyObjectResult>
```
