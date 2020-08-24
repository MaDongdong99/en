# Create high availability Application Application Load Balancer across availability zones

## Preparation and planning

- Networking preparation

	Plan for Application Application Load Balancer, and region, availability zone, virtual private cloud, etc. of VM and containers as backend server in advance, according to business deployment needs.

- Server preparation

	It is necessary to create VM and containers for carrying business traffic in advance, and ensure that the ports needed for listening are opened, and that security groups and ACL policies are properly configured.

Note: Only when the available zone of the Application Application Load Balancer instance is created, VM and containers under the availability zone can be configured as the backend service. For example, when the Application Application Load Balancer is in Availability Zone A, Availability Zone B, VM and containers in Availability Zone A, Availability Zone B can be configured to conduct traffic forwarding.
	
## Create Application Application Load Balancer instance


1. Open the Application Application Load Balancer resource list page through the console menu - Application Application Load Balancer, and click **Create** to create a new Application Application Load Balancer instance.

	![ALB创建实例设置](../../../../image/Networking/ALB/ALB-067.png)


1. Select the corresponding region: cn-north-1, Availability Zone: Availability Zone A, Availability Zone B.

	![ALB选择地域设置](../../../../image/Networking/ALB/ALB-068.png)

1. Selection Virtual Private Cloud, Subnet, Security Group, Associate EIP, and select Billing Method, Bandwidth.

	![ALB网络设置](../../../../image/Networking/ALB/ALB-069.png)

1. Fill in Application Application Load Balancer Name, Description.

	![ALB基本设置](../../../../image/Networking/ALB/ALB-070.png)

- Confirm Configuration Information, Click **Purchase Now**.

	![ALB购买设置](../../../../image/Networking/ALB/ALB-071.png)

- Confirm order information and complete payment, create a Application Application Load Balancer instance

	![ALB支付设置](../../../../image/Networking/ALB/ALB-072.png)

- Refresh Application Application Load Balancer list, view the newly created Application Application Load Balancer instance.

	![ALB查看设置](../../../../image/Networking/ALB/ALB-073.png)

- Click **Add listener** on the right side of the list to open listener page.

	![ALB监听设置](../../../../image/Networking/ALB/ALB-074.png)

- Create an HTTP listener

	Click **Create a listener** to create a listener.

	Frontend listening configuration:

	1. Configure Listening Protocol as HTTP, Port 80;

	2. Idle connection timeout: set idle connection timeout time;

	![ALB新建监听器设置](../../../../image/Networking/ALB/ALB-075.png)

- Backend forwarding configuration:

	1. Backend service by fault: May create a new backend service or select an existing backend service;

	2. Backend service name: Define backend service name;

	3. Backend Protocol: Display the corresponding default protocol according to the Listening Protocol

	4. Port: Define backend forwarding port;

	5. Scheduling algorithm: Select according to business needs, and specify it as weighted round robin;

	6. Session persistence: Turn on; timeout: define timeout time of cookie, use default value 0, represent the same life cycle as the browser;

	7. Get real IP: Turn on by default: In such case, real IP of client can be obtained via header fields of X-Forwarded-For;

	8. Get HTTP header field: Tick according to business needs.

	![ALB后端转发设置](../../../../image/Networking/ALB/ALB-076.png)

- Health check:

	Select health check method as: http

	Configure related parameters according to business needs:

	![ALB健康检查设置](../../../../image/Networking/ALB/ALB-094.png)

- Add server group:

	Select virtual server group, availability group according to business needs.

	![ALB添加服务器组设置](../../../../image/Networking/ALB/ALB-049.png)

- Add server to the virtual server group:

	If there is no available virtual server group, click "create new virtual server group" to create a new virtual server group. VM and containers can be selected to define the port and weight of the instance;

	Note: Only VM and container resources in the same Availability Zone, virtual private cloud with Application Application Load Balancer can be selected.

	![ALB虚拟服务器组添加成员设置](../../../../image/Networking/ALB/ALB-050.png)

	Thus, a Application Application Load Balancer HTTP listener configuration across the Availability Zones is completed. When A single Availability Zone (such as Availability Zone A) fails, the Application Application Load Balancer will forward the traffic to Availability Zone B to ensure the normal operation of business.

	
	​			
	​			
	​			
	​			
