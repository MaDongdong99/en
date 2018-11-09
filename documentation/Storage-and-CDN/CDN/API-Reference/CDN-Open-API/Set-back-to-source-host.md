# **Set Back-to-origin Host**

## **1. Description**

Set Back-to-origin Host

## **2. Request Parameter**

| **Name**   | **Type** | **Compulsory or Not ** | **Description**                                                     |
| ---------- | -------- | ------------ | ------------------------------------------------------------ |
| username   | String   | Yes           | JD User Name pin                                               |
| signature  | String   | Yes           | User Signature, verify user's identity information through md5 method to ensure information security.  md5=date+username+secret key SecretKey date: format is yyyymmddusername: JD user name pin secret key: example agreed between the Parties: such as current date 2016-10-23, user pin: jcloud_00, user secret key SecretKey: e7a31b1c5ea0efa9aa2f29c6559f7d61, then the signature is MD5(20161023jcloud_00e7a31b1c5ea0efa9aa2f29c6559f7d61) |
| domain     | String   | Yes           | Accelerated Domain Name                                                     |
| sourceHost | String   | Yes           | Back-to-origin Host                                                     |

## **3. Return Parameter** 

| **Name**   | **Description**                                                  |
| -------- | --------------------------------------------------------- |
| status   | Result status means whether the API request is successful or not, 0 means successful, others means failure|
| msg      | Note information, e.g. the reasons why task sending fails, etc.                             |
| data     | Return Data                                                   |

## **4. Call Example**

- ### **Request Address**

http://opencdn.jcloud.com/api/setReferHost

- ### **Request Example**

 * Json Format

```
{
“username” :“test_user”, 
“signature” :“d00f58f89e8cd55dc080aec0d8051845”, 
“domain” :“www.a.com”, 
“sourceHost” :“sourcehost1.www.a.com”
 }
```

- ### **Return Example**

•        Json Format

```
{
  "status": 0,
  "msg": “Successful",
  "data": "www.a.com"
}
```
