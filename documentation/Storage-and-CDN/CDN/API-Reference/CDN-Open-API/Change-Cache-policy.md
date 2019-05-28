# **Cache Policy Change**

## **1. Description**

Cache Policy Change (changeCache/{status})

## **2. Request Parameter**

| **Name**   | **Type** | **Compulsory or Not ** | **Description**                                                     |
| --------- | -------- | ------------ | ------------------------------------------------------------ |
| username  | String   | Yes            | JD User Name pin                                                |
| signature | String   | Yes           | User Signature, verify user's identity information through md5 method to ensure information security.</br> md5=date+username+secret key SecretKey; date: format is yyyymmdd; username: JD user name pin secret key: agreed between the Parties;</br> example: such as current date 2016-10-23, user pin: jcloud_00, user secret key SecretKey: e7a31b1c5ea0efa9aa2f29c6559f7d61, then the signature is MD5(20161023jcloud_00e7a31b1c5ea0efa9aa2f29c6559f7d61) |
| domain         | String   | Yes           | Accelerated Domain Name                                                     |
| cacheType  | String   | No           |  Cache Type: 0 means no cache, 1 means customization                        | By default is customized cache        |
| weight    | String   | Yes            | Weight, weight cannot be repeated, only one can be created when having the same weights                   |
| content   | String   | Yes           | Cache Policy Contents                                                 |
| ttl       | int      | Yes           | Expiry Time, time seconds                                             |
| configid   | int      | No         |  The request parameter must be configid when calling update and delete and the configuration id must be cached                                        |

## **3. Return Parameter**

| **Name**   | **Description**                                                  |
| -------- | --------------------------------------------------------- |
| status   | Result status means whether the API request is successful or not, 0 means successful, others means failure|
| msg      | Note Information                       |
| data     | Return Data                                                   |

 

## **4. Call Example**

- ### **Request Address**

Set cache configuration: https://opencdn.jcloud.com/api/changeCache/add
Change cache configuration: https://opencdn.jcloud.com/api/changeCache/update
Delete cache configuration: https://opencdn.jcloud.com/api/changeCache/delete

- ### **Request Example**

curl Request Example:

```
 curl -H "Content-type: application/json" -X POST -d ‘{"username":"test_user","signature":"914a3f412fd9bc1eec14bb5eb104d253","domain" :"www.a.com", "weight" :"1", "ttl" :"7200", "content" :".jpg"}’ http://opencdn.jcloud.com/api/changeCache/add
```

* json Format

```
https://opencdn.jcloud.com/api/changeCache/add
{
    "username" :"test_user",
    "signature" :"d00f58f89e8cd55dc080aec0d8051845",
    "domain" :"www.a.com",
    "weight" :"1",
    "ttl" :"7200",
    "content" :".jpg"
 }
```

- ### **Return Example**

* json Format

```
{
    "status": 0,
    "msg": "Successful",
    "data": {
        "domain": "www.a.com",
        "configId": "12310"
    }
}
```