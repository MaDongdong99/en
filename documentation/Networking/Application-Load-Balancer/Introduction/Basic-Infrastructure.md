# Basic architecture

- The Application Load Balancer provides four-layer and seven-layer load listening service, so as to realize traffic forwarding under TCP Protocol, TLS Protocol, HTTP Protocol and HTTPS Protocol.
- The Application Load Balancer adopts cluster for deployment, so as to improve service availability through device redundancy and eliminate device single point failure.

![负载均衡基础架构](../../../../image/Networking/ALB/ALB-002.png)

## Components

- Application Load Balancer instance

Before using the Application Load Balancer service, it needs to purchase, create Application Load Balancer instance, one Application Load Balancer instance can be set up with multiple listeners, multiple backend services, multiple virtual server groups, and can be attached with multiple availability groups.

- Listener

Before performing traffic loading, it needs to set up at least one listener, designate the listening protocol/port et.

- Backend service

It is used for providing management module for forwarding, scheduling policy from Application Load Balancer to backend server, including forwarding protocol/port, scheduling algorithm, session persistence and forwarding backend server, etc.

- Virtual server group

A set of VM or container resources receiving access request is managed by the virtual server group. The virtual server group can be combined with auto scaling for use so as to realize auto expansion and contraction of VM, but the dispersion capacity of machine of AS is relatively weak, paying no attention to high availability dispersion mechanism across rack dimensions.

- Availability Group

Availability Group is the Virtual Machine logic set provided by JD Cloud, which may support auto scaling across racks, across AZ according to the machine template designated by the user so as to distribute Virtual Machines in dispersion to the physical resources separately isolated. When hardware or power failure occurs, only the Virtual Machines in Availability Group can be affected, the business is still in available status.

- Forwarding Rules Group

The forwarding rules group is a logical set of forwarding rules. Seven-layer listening supports association with the forwarding rules group to forward the traffic to different backend servers for processing based on domains and paths requested by URL.

## High reusability architecture

![高复用架构](../../../../image/Networking/ALB/ALB-003.png)

- Listeners of multiple different protocol types (HTTP/HTTPS/TCP/TLS) can be set under one Application Load Balancer, and listeners in the multiple same protocol types but under different server port numbers can be also set;

- Multiple listeners under the same Application Load Balancer can be reused to associate with the same backend service;

- Multiple backend services under the same Application Load Balancer can be reused to associate with the same backend server group/availability group;

- Multiple listeners under the same Application Load Balancer can be reused to associate with the same forwarding rules group;

- The same virtual server (machine/container) can be registered to the same virtual server group through different ports;

- The same virtual server (machine/container) can be registered to different virtual server groups;

- The same availability group can be attached to multiple backend services of the same Application Load Balancer;

- The same availability group can be attached to backend services of multiple Application Load Balancers.

	Note: The virtual server group can be only added with servers that are on the same Virtual Private Cloud as the associated Application Load Balancer instance.

## Shunting principles

An external access request is distributed to the backend server by the Application Load Balancer Instance according to the relevant policies and forwarding rules for processing. At present, the shunting type supported by the Application Load Balancer includes: weighted round robin, weighting least connection and weighted source IP. Round robin means distributing connection request one by one by order to the backend service instance, weighted round robin means distributing the round times according to the weight ratio of instance. The least connection distributes requests according to the minimum count of active connections between Application Load Balancer and each backend service instance, the weighted least connection finally guarantees the ratio of the count of active connections between Application Load Balancer and backend services to be consistent with the weight ratio. Source IP is to hash according to the requested source IP addresses where requests of the same source IP will be distributed to the same backend service instance for processing. Weighted source IP is to guarantee that the proportion of the source IP count corresponding to the backend service instance distributed by the Load Balancer in all of the requested source IP count is consistent with the weight ratio.

![分流原理](../../../../image/Networking/ALB/ALB-043.png)

## Session persistence principles

Session persistence is also called as Sticky Sessions or Session affinity. Session persistence means a functional mechanism on the Application Load Balancer, which distributes data while guaranteeing that relevant access requests from the same client can be distributed to the same server.

For the seven-layer HTTP/HTTPS Protocol session persistence, the Application Load Balancer is in charge of inserting cookie, there is no need for modification of backend server. When the client makes the first request, HTTP request (without cookie) of the client enters the Application Load Balancer, the Application Load Balancer selects one set of backend server according to the scheduling algorithm policy and sends the request to the server; HTTP response (without cookie) of the backend server is sent back to the Application Load Balancer. Then, the Application Load Balancer will insert the HTTP response into cookie (save associated information of backend server) and return the HTTP response to the client.

When the customer request occurs once again, customer HTTP request (with cookie inserted by the last Application Load Balancer) enters the Application Load Balancer, then, the Application Load Balancer reads out the session persistence value in cookie, and sends the HTTP request (with cookie same as above) to the designated server, the backend server responds to the request; because the cookie will not be written in the server, the HTTP response will not carry cookie, when the HTTP response enters the Application Load Balancer, the Application Load Balancer will write cookie after refresh aging time in the HTTP response and return the HTTP response to the client.

![会话保持](../../../../image/Networking/ALB/ALB-044.png)

## Relevant references

- [Product advantage](../Introduction/Benefits.md)
- [Product function](../Introduction/Features.md)
- [Price overview](../Pricing/Price-Overview.md)
- [Billing rules](../Pricing/Billing-Rules.md)
- [Create instance](../Getting-Started/Create-Instance.md)
- [Create virtual server group](../Operation-Guide/TargetGroup-Management.md)
- [Configure listening policy](../Operation-Guide/Listener-Management.md)
- [Manage rear end service and view health status of service instance](../Operation-Guide/Backend-Management.md)
- [View monitoring information](../Operation-Guide/Monitoring.md)



