# **Bandwidth Query**

## **1. Description**

Bandwidth Query

## **2. Request Parameter**

| **Name**   | **Type** | **Compulsory or Not ** | **Description**                                                     |
| ---------- | -------- | ------------ | ------------------------------------------------------------ |
| username   | String   | Yes           | JD User Name pin                                                |
| signature  | String   | Yes           | User Signature, verify user's identity information through md5 method to ensure information security.</br> md5=date+username+secret key SecretKey; date: format is yyyymmdd; username: JD user name pin secret key: agreed between the Parties;</br> example: such as current date 2016-10-23, user pin: jcloud_00, user secret key SecretKey: e7a31b1c5ea0efa9aa2f29c6559f7d61, then the signature is MD5(20161023jcloud_00e7a31b1c5ea0efa9aa2f29c6559f7d61) |
| domain     | String   | Yes           | Domain name to be queried, support query of multiple domain names, parameter example "www.a.com,www.b.com"; When domain is empty, it queries the total bandwidth of all domain names under this username |
| start_time | String   | Yes           | Time Format: yyyy-mm-dd hh:mi Reference Example 2016-12-14 07:00; the time span for query cannot be greater than 31 days  |
| end_time   | String   | No           | Not a compulsory parameter; if no parameter is uploaded, it is current time by default                             |

## **3. Return Parameter**

| **Name** | **Description**                       |
| -------- | ------------------------------ |
| status   | Result status 0, refresh successful, others failure|
| msg      | Note Information                       |
| data     | Return Data                       |

## **4. Call Example**

- ### **Request Address**

https://opencdn.jcloud.com/api/bandwidth

- ### **Request Example**

```
https://opencdn.jcloud.com/api/bandwidth
{
    "username" :"test_user",
    "signature" :"d847267fc702273abf394dd0c3128d64",
    "domain" :"www.a.com,www.b.com",
    "start_time" :"2016-12-14 07:00",
    "end_time" :"2016-12-14 12:59"
 }
```

- ### **Return Instructions**

* json Format

```
{
"status": 0,//0 means this request succeeded
"data": [
{
"domain": "DOMAIN",//Queried domain name, do not include http://
"data": [
[
TS, //Time Stamp
BANDWIDTH,//Bandwidth, Mbps
],
],
},
]
}
```

- ### **Return Example**

```
{
  "status": 0,
  "msg": "Successful",
  "data": [
    {
      "domain": "www.a.com",
      "data": [
        [
          1480989900,
          1
        ],
        [
          1480990200,
          301
        ],
        [
          1480990500,
          601
        ],
        [
          1480990800,
          901
        ]
      ]
    },
    {
      "domain": "www.b.com",
      "data": [
        [
          1480989900,
          100
        ],
        [
          1480990200,
          400
        ],
        [
          1480990500,
          700
        ],
        [
          1480990800,
          1000
        ]
      ]
    }
  ]
}
```