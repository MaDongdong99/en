## VPC Attachment

### Basic Concept

VPC Attachment, is the service provided by JD Cloud, which is used to Get through the connection between JD Public Cloud VPC and Border Gateway, and realize the interconnection of single or multiple VPCs of JD Cloud and your IDC own network at the Intranet level, or your convenient connection among multiple VPCs in the same region on JD Cloud to provide users with rich and flexible connectivity solutions between the Hybrid Cloud and Isolation Network.

### Features

- Connect VPC to border gateway: Get through the connection between JD Public Cloud VPC and border gateway, and then use the transfer capability of border gateway to realize high-speed interconnection among one VPC and multiple VPCs in the same region or among VPN connection/private virtual interface/hosted private virtual interface.

- Connection method of VPC and Border Gateway: Now, VPC Attachment supports interconnection between VPC and Border Gateway in the same region. One VPC Attachment can be created for the same VPC and the same Border Gateway. The same VPC can create different VPC Attachments with multiple different Border Gateways, one Border Gateway support the creation of different VPC Attachments with multiple different VPCs.

- Route Transmission Feature: Dynamic transmission with two-way routing can be realized between VPC Route Table and Border Gateway Route Table by VPC Attachment.

  VPC->Route transmission to a border gateway: When creating VPC attachment based on border gateway, if "VPC All Segment" or "Specify Subnet Segment" is selected in the transmission of VPC segment, it is the automatic route transmission method. The Border Gateway Transmission Route Table will automatically add or delete route table items that reach the relevant subnet based on the configured subnet scope, the route prefix is the subnet segment, and the Next Hop is the VPC Attachment connecting the specified VPC and the Border Gateway. For more content of Border Gateway Route Table configuration route transmission, refer to [VPC Attachment Operation Manual](../../Operation-Guide/Border-Gateway-Management/VPC-Attachment-Configuration.md).

  Border Gateway->Route transmission to VPC direction: When VPC Route Table configures the route transmission, fill in the Source Border Gateway and route transmission range for route transmission; the system will automatically add the routing rules that conform to the transmission range in the valid route table of the border gateway to the VPC route table, and the Next Hop points to the source border gateway. For more content of VPC Route Table configuration route transmission, refer to [VPC Route Table Operation Manual](https://docs.jdcloud.com/en/virtual-private-cloud/route-table-configuration).;

- Static Route Configuration: VPC and Border Gateway can achieve connection between VPC and Border Gateway by configuration of static route.

- Network High Performance: The performance of single VPC Attachment can be up to 10Gbps.
