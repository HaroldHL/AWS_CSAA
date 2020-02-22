# Chapter 3: EC2&EBS

**Amazon Elastic Compute Cloud \(Amazon EC2\)**

— Basic Conception

* Amazon EC2 allows you to acquire compute through the launching of virtual servers called **instances**.
* Two Keys
  * Instance Type
  * AMI

**Instance Types**

* Virtual CPUs \(vCPUs\)
* Memory
* Storage \(size and type\)
* Network performance

**Amazon Machine Images \(AMIs\)**

* The Operating System \(OS\) and its configuration
* The initial state of any patches
* Application or system software

There are _four sources_of AMIs:

* **Published by AWS**
* **The AWS Marketplace**
* **Generated from Existing Instances**
* **Uploaded Virtual Servers**

**Securely Using an Instance**

* **Addressing an Instance**
  * Public Domain Name System \(DNS\) Name
  * Public IP
  * Elastic IP
* **Initial Access**  \(public-key cryptography to encrypt and decrypt login information\)
* **Virtual Firewall Protection** \( _security groups_\)

**The Lifecycle of Instances**

* Launching
* Bootstrapping \( configure instances and install applications programmatically when an instance is launched. \)
  * Applying patches and updates to the OS
  * Enrolling in a directory service
  * Installing application software
  * Copying a longer script or program from storage to be run on the instance
  * Installing Chef or Puppet and assigning the instance a role so the configuration management software can configure the instance
* VM Import/Export \( only export previously imported Amazon EC2 instances / Instances launched within AWS from AMIs cannot be exported\)
* Instance Metedata\(configure or manage the running instance/**AWS API**\)
  * The associated security groups
  * The instance ID
  * The instance type
  * The AMI used to launch the instance
* Managing Instances

  | **Key** | **Value** |
  | :--- | :--- |
  | Project | TimeEntry |
  | Environment | Production |
  | BillingCode | 4004 |

* Monitoring Instances \(via CloudWatch\)
* Modifying an Instance
* Security Groups
* Termination Protection

**Architectures with Different Pricing Models**

**For Exam**,it’s important to know how to take advantage of the different pricing models to create a cost-efficient architecture.For instance, a website that averages 5,000 visits a day, but ramps up to 20,000 visits a day during periodic peaks, may purchase two **Reserved Instances** to handle the average traffic, but depend on **On- Demand Instances** to fulfill compute needs during the peak times.

**Instance Stores**

— The size and type of instance stores available with an Amazon EC2 instance depend on the **instance type**

Instance stores are included in the cost of an Amazon EC2 instance，so they are a very **cost- effective** solution for appropriate workloads. **Temporary** & Data is Lost when:

* The underlying disk drive fails.
* The instance stops \(the data will persist if an instance reboots\).
* The instance terminates.

——————————————————————————————————————————————————

## **Amazon Elastic Block Store \(Amazon EBS\)**

— Basic Coception

provides persistent block-level storage volumes for use with Amazon EC2 instances

**EBS Volumes Types**

* Magnetic Volumes
* General-Purpose SSD\(they cost the lowest per gigabyte\)
  * System boot volumes
  * Small- to medium-sized databases
  * Development and test environments
* Provisional IOPS SSD

