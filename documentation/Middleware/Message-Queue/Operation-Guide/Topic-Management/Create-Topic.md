# Create Topic
  You can create topic on the Topic Management page.

## Prerequisites
- You have created a JD Cloud account and finished real-name verification. Your account is usable and doesn't exist in the black list. If you don't have an account, please [Register](https://accounts.jdcloud.com/p/regPage?source=jdcloud%26ReturnUrl=%2f%2fuc.jdcloud.com%2fpassport%2fcomplete%3freturnUrl%3dhttp%3A%2F%2Fuc.jdcloud.com%2Fredirect%2FloginRouter%3FreturnUrl%3Dhttps%253A%252F%252Fwww.jdcloud.com%252Fhelp%252Fdetail%252F734%252FisCatalog%252F1), and [verify real-name](https://uc.jdcloud.com/account/certify).
- Because the Billing Type of the product is charged by amount, please confirm that your account cannot be overdue.

## Note
- By default, users can only create up to 10 topics in one region. If necessary, they can increase the number by opening ticket.
- In the region: public network (North China), Message Queue Service can only be used for testing (public network can be directly accessed); please do not use it in the production environment, and the product's service level agreement shall not be committed.
- The production environment is recommended to be in other regions (Message Queue Service public network is inaccessible; it can be directly accessed within VPC).


## Procedure
### 1. Click **Create** in the Topic Management page

In the left menu of the console, click **Create** in [Middleware] - [Message Queue] - Management interface of [JCQ-Topic]
 ![创建topic步骤1](../../../../../image/Internet-Middleware/Message-Queue/创建topic-01.PNG)

### 2. Complete Topic Information and click **Create**.

Refresh pages to finish new topic creation
 ![创建topic步骤2](../../../../../image/Internet-Middleware/Message-Queue/创建topic-02.png)  
I. The topic name can be entered according to the prompt information, and cannot be modified.  
II. Message type consists of common message and global sequential message:  

- Common message: Cannot guarantee first in first out (FIFO) ordered consumption, including general messages and delayed messages.
- Global ordered messages: The production and consumption of messages are carried out according to the publishing order of messages (FIFO).  

III. You should enter the remarks according to the requirements, and cannot exceed 255 bytes.
