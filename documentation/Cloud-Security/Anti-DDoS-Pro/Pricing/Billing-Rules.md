# Billing Rules

Anti-DDoS Pro supports two billing types:

* Monthly Package
* Monthly Package + Pay-As-You-Go

## Monthly Package
### Introduction
If you only purchase basic protection, you will be charged with monthly package as the Pay-As-You-Go mode.
In this way, Anti-DDoS Pro only provides fixed protective capability on the basis of your chosen package.

### Example
When the elastic protection is selected 0, the elastic protection is not activated.
As shown, the user purchased the 5G basic protection of the three operator lines only, but didn’t enable the elastic protection.
![IP高防保底计费](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/billing3.png)
Example: When the attack<=5G, the Anti-DDoS Pro system provides protection.
    When the attack>5G, the instance has exceeded the maximum protection peak value of the basic protection. Because the user has not purchased elastic protection, the protection IP will be treated by the black hole, causing affect to the business.





## Monthly Package + Pay-As-You-Go
### Introduction
If you have purchased elastic protection, you will be charged based on the monthly package.
The elastic protection part is charged daily according to the larger actual billing interval of the Attack Peak Value exceeding the minimum protective capability (Gbps) or CC protective capability (QPS) of the day before,
then a bill of Pay-As-You-Go will be generated.
If the attack does not exceed the defense peak value of basic protection, you will not be charged for the elastic protection.

### Example
It is recommended that the users adopt the mixed billing method of basic protection and elastic protection to fight against the DDoS attack.
Take the following figure as an example: the user purchases 5Gbps of one-month basic protection and 10Gbps of elastic protection in a mixed billing method.
![IP高防弹性计费](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/billing4.png)
When the attack traffic does not exceed 5G, there will be no charge of elastic protection. When the attack traffic exceeds 5G, the Anti-DDoS Pro will still provide attack protection, with maximum protection bandwidth being 15G. The cost will be charged the day after according to the interval in which the actual bandwidth exceeds the elastic protection.
Example: If the maximum Attack Peak Value is 3G on November 10, the billing method of the monthly package does not require additional elastic billing charges.
   If the maximum Attack Peak Value is 13G on November 11, then on November 12, there will be charge of elastic interval (0Gbps
