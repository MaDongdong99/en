# Update DNS Resolution

After this step is completed, all users' access traffic will be forwarded back to the user's Origin Server after being through Anti-DDoS Pro.

## Precondition
- The Anti-DDoS Pro has been successfully purchased and the billing status is normal. <Br/>
- All Forwarding Settings have been completed and been verified to take effect.

## Operation Steps
1. Log in [Anti-DDoS Pro Console](https://ip-anti-console.jdcloud.com/instancelist).
2. On the "Instance List" page, select the target instance, then click **Instance Name** or **Forwarding Setting** to enter the Instance Details page. Copy the cname value to be modified in the web service or non-web service forwarding rules. <Br/>
Take non-web service forwarding rules as an example, find the cname to be copied at the red box as follows:
![修改DNS](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/update%20dns%2005.png)
3. At the provider of domain, you need to modify the domain name resolution configuration to resolve the domain name to the IP of Anti-DDoS Pro.
Take the "JD Cloud DNS" of JD Cloud & AI as an example, on **Console** –> **Domain & License** –> **JD Cloud DNS**, enter JD Cloud [JD Cloud DNS Console](https://dns-console.jdcloud.com/list). <Br/>
![Modify DNS](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/update%20dns%2006.png)<Br/>
Find the domain name to be resolved, as follows:
![Modify DNS](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/update%20dns%2007.png)<Br/>
Click to enter the resolution configuration:
![Modify DNS](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/update%20dns%2008.png)<Br/>
Change the record value to the cname address of Anti-DDoS Pro.


## Special Instructions
- If the **Defense/Back-to-origin** status in the forwarding rules is back-to-origin, the access traffic shall be directly resolved to the origin server IP address.


## Related Reference
- [Start Overview](Overview.md)
- [Create Instance](Create-Instance.md)
- [Non-Web Service Rule](Non-Web-Service-Forwarding-Rule.md)
- [Web Service Rule](Web-Service-Forwarding-Rule.md)
- [Release Back-to-origin IP](Whitelist-local-IP-subnet.md)
- [Billing Rules](../Pricing/Billing-Rules.md)
