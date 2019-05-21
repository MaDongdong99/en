# **Query Accelerated Domain Name**

## **1. Description**

Query Accelerated Domain Name

## **2. Request Parameter**

| **Name**   | **Type** | **Compulsory or Not** | **Description**                                                     |
| ---------- | -------- | ------------ | ------------------------------------------------------------ |
| username   | String   | Yes           | JD User Name pin                                                |
| signature | String   | Yes           | User Signature, verify user's identity information through md5 method to ensure information security.</br> md5=date+username+secret key SecretKey; date: format is yyyymmdd; username: JD user name pin secret key: agreed between the Parties;</br> example: such as current date 2016-10-23, user pin: jcloud_00, user secret key SecretKey: e7a31b1c5ea0efa9aa2f29c6559f7d61, then the signature is MD5(20161023jcloud_00e7a31b1c5ea0efa9aa2f29c6559f7d61) |
| domain     | String   | No           | Fuzzily match accelerated domain name                                             |
| pageNumber | int      | No           | Query the paging page number, 1 by default if not uploaded                                    |
| pageSize   | int      | No           | Query the paging number, 10 by default if not uploaded                                   |
| type       | String   | No          | Domain service resource type, currently only supports: web means image small files, download means large file download, vod means video files, dynamic means dynamic acceleration; (api interface is adopted for CDN live) |
| status     | String   | No           | Status, search all the domains if not uploaded, 0 (search the suspended domains), 1 (search the running domains), 4 (search the configuring domains), 5 (search the domains being audited), 6 (search the unapproved and rejected domains), 7 (search the blocked domains) |

## **3. Return Parameter**

| **Name** | **Description**                                                     |
| -------- | ------------------------------------------------------------ |
| status   | Result status, means whether the API request is succeeded, 0 means succeeded, others means failed    |
| msg      | Note information, e.g. the reasons why task sending is failed, etc.                             |
| data     | Domain Name Information Array                                                 |
| domain   | Accelerated Domain Name                                                     |
| cname    | cname                                                        |
| type     | Domain service resource type, currently only supports: small image file, large file download, video file, dynamic acceleration; (api interface is adopted for CDN live) |
| status   | The enabling application status of the domain, running, auditing, disapproved, configuring, stopped, blocked   |

## **4. Call Example**

- ### **Request Address**

https://opencdn.jcloud.com/api/queryDomains

- ### **Request Example**

curl Request Example: 

```
curl -H “Content-type: application/json” -X POST -d ‘{“username”:“test_user”,“signature”:“914a3f412fd9bc1eec14bb5eb104d253”,“pageNumber”:1,“pageSize”:10}’ https://opencdn.jcloud.com/api/queryDomains
```

* json Format

```
https://opencdn.jcloud.com/api/queryDomains
{
    "username" :"test_user",
    "signature" :"b036e6094db32b5a5abc47e6be426c50",
    "pageNumber":1,
    "pageSize":10
   
 }
```

- ### **Return Example**

* json Format

```
{
    "status": 0,
    "msg": "Successful",
    "data": {
        "total": 10,
        "domains": [
            {
                "cname": "www.a.com.s.galileo.jcloud-cdn.com",
                "domain": "www.a.com",
                "status": "Configuring",
                "type": "Image Small File"
            },
            {
                "cname": "www.b.com.s.galileo.jcloud-cdn.com",
                "domain": " www.b.com ",
                "status": "Configuring",
                "type": "Image Small File"
            }
            ]
    }
}
```

 