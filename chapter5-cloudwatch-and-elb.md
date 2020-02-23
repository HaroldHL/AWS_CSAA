# Chapter5: CloudWatch&ELB

**Elastic Load Balancing, Amazon CloudWatch**

Basics:

* ELB:
  * a highly available service that distributes traffic across Amazon Elastic Compute Cloud \(Amazon EC2\) instances and includes options that provide flexibility and control of incoming requests to Amazon EC2 instances.
* _CloudWatch_
  * a service that monitors AWS Cloud resources and applications running on AWS
* _Auto Scaling_
  * a service that allows you to maintain the availability of your applications

**Elastic Load Balancing**

* A load balancer is a mechanism that automatically distributes traffic across multiple Amazon EC2 instances.
* distribute traffic across a group of Amazon EC2 instances in one or more _Availability Zones_

Advantages of ELB

* it scales in and out automatically
* seamlessly integrates with the Auto Scaling service
* secure, working with VPC

Types of Load Balancers

* **Internet-Facing Load Balancers**
  * It takes requests from clients over the Internet and distributes them to Amazon EC2 instances that are registered with the load balancer.
* **Internal Load Balancers**
* **HTTPS Load Balancers**
  * create a load balancer that uses the SSL/Transport Layer Security \(TLS\) protocol for encrypted connections \(also known as _SSL offload_\)

**Configuring Elastic Load Balancing**

* Cross-Zone Load Balancing
* Connection Draining
* Proxy Protocol
* Sticky Sessions
* Health Checks

**Amazon CloudWatch**

* monitor CPU utilization
* perform a PUT request to push that metric into Amazon CloudWatch
* supports monitoring and specific metrics for most AWS Cloud services

