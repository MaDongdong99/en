# **Domain Name Management**

**Create Domain**

 1. Enter the **Domain Name List** page in the CDN customer console; click "Add Domain Name";           

![image.png](https://img1.jcloudcs.com/cms/b5b15af8-d4c9-4806-a050-e59c81ddbcf120180423142138.png)

2. Fill in or select the following information in the "Add Accelerated Domain Name" page that opens, and then click the "OK" button.

* Accelerated domain name: Fill in the information of the domain name, of which the content needs to be distributed and accelerated.

  Please complete the ICP filing of the domain name with the communications administration and then conduct this domain name adding configuration;

  Domain name filling characters only support 26 English letters, 10 Arabic numerals and the horizontal bar "-"'*’;

  Support Extensive Domain, do not support the domain addition of domain and sub-domain with the same content. For example, if you have added the Extensive Domain *.b.a.com, it is not supported to add c.b.a.com or b.a.com;

  Supporting adding up to 100 accelerated domain names. If there are more domain name acceleration demands, please open online tickets.

* Business type: Please select the appropriate business type based on the domain name content.

  Image & small file: Applicable to scenarios of accelerating static websites, images and files smaller than 10MB;

  Large file download: Applicable to scenarios of distributing files larger than 20MB;

  Video file: Applicable to scenarios of accelerating on-demand audios and videos.

* Daily peak bandwidth of the business: Please estimate the daily peak bandwidth. For large file download and video file acceleration business, please fill in the file size information, so that we can reasonably allocate resources for you.

* Back-to-source mode: Please select IP back-to-source, domain name back-to-source or OSS back-to-source according to actual needs, fill in the origin server IP address and origin server domain name, and select the bucket information of OSS. JD Cloud CDN supports multi-IP load balancer back-to-source, and multi-IP, multi-domain name backup back-to-source, please fill in the back-to-source configuration according to actual needs.

![image.png](https://github.com/jdcloudcom/cn/blob/cdn-new/image/CDN/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%9B%9E%E6%BA%90host.png)

**Accelerated Domain Recycling Rule**

* If the accelerated domain hasn’t have any access traffics for more than 90 days (including the status of "normal running"), the platform will automatically "stop" the domain, but still keep records related to such accelerated domain; if you need to use the accelerated domain, please "run" it.
* The accelerated domain has been in the "Stopped" status (including the status of "Reviewing") for more than 120 days, and the system will automatically delete records related to the domain; if you still need to make CDN acceleration to the domain, please add the domain again.
