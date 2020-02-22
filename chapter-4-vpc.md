# Chapter 4: VPC

**Amazon Virtual Private Cloud \(Amazon VPC\)**

— a custom-defined virtual network

— _A strong understanding of Amazon VPC topology and troubleshooting is required to pass the exam_

With VPC, you can

* selecting your own IP address range
* creating your own _subnets_
* configuring your own route tables, network gateways, and security settings
* two different networking platforms
  * EC2-Classic 
  * EC2-VPC

An Amazon VPC consists of the following components:

* Subnets
  * a segment of an Amazon VPC’s IP address range
  * Subnets reside within one Availability Zone and cannot span zones/remember that one subnet equals one Availability Zone
* Route tables
* Dynamic Host Configuration Protocol \(DHCP\) option sets
  * sets element of an Amazon VPC allows you to direct Amazon EC2 host

    name assignment to your own resources
* Security groups
  * a virtual stateful firewall that controls inbound and outbound traffic to Amazon EC2 instances
* Network Access Control Lists \(ACLs\)
  * acts as a stateless firewall on a subnet level

An Amazon VPC has the following optional components:

* Internet Gateways \(IGWs\)
  * IGW provides a target in your Amazon VPC route tables for Internet-routable traffic
  * network address translation for instances that have been assigned public IP addresses.
* Elastic IP \(EIP\) addresses
  * a static, public IP address in the pool for the region
* Elastic Network Interfaces \(ENIs\)
* Endpoints
  * enables you to create a private connection between your Amazon VPC and another AWS service without requiring access over the Internet or through a NAT instance, VPN connection, or AWS Direct Connect
* Peering
  * a networking connection between two Amazon VPCs
* Network Address Translation \(NATs\) instances and NAT gateways
  * an AWS-managed service that is designed to accept traffic from instances within a private subnet, translate the source IP address to the public IP address of the NAT gateway, and forward the traffic to the IGW
* Virtual Private Gateway \(VPG\), Customer Gateways \(CGWs\), and Virtual Private Networks \(VPNs\)
  * VPN concentrator on the AWS side of the VPN connection between the two networks

