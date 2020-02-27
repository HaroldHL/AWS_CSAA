# Chapter 11: key AWS services



**key AWS services**

* Storage and Content Delivery
  * **Amazon CloudFront** is a CDN service.
    * **Distributions** : you start by creating a _distribution_, which is identified by a DNS domain name such as d111111abcdef8.cloudfront.net.
    * **Origins**:specify the DNS domain name of the _origin_—the Amazon S3 bucket or HTTP server—from which you want Amazon CloudFront to get the definitive version of your objects \(web files\)
    * **Cache Control**:Once requested and served from an edge location, objects stay in the cache until they expire or are evicted to make room for more frequently requested content. By default, objects expire from the cache after 24 hours.
  * **AWS Storage Gateway**
    * **Gateway-Cached Volumes** 
      * expand your local storage capacity into Amazon S3;a single gateway can support up to 32 volumes for a maximum storage of 1 PB.
      * All Gateway-Cached volume data and snapshot data is transferred to Amazon S3 over encrypted Secure Sockets Layer \(SSL\) connections
    * **Gateway-Stored Volumes** 
      * store your data on your on-premises storage and asynchronously back up that data to Amazon S3
      * While each volume is limited to a maximum size of 16TB, a single gateway can support up to 32 volumes for a maximum storage of 512TB.
    * **Gateway Virtual Tape Libraries \(VTL\)** 
      * The _VTL_ interface lets you leverage your existing tape-based backup application infrastructure to store data on virtual tape cartridges that you create on your Gateway-VTL.
* Security
  * **AWS Directory Service**
    * AWS Directory Service for Microsoft Active Directory \(Enterprise Edition\), also referred to as Microsoft AD
    * Simple AD
    * AD Connector
  * **KMS**
    * A service enabling you to generate, store, enable/disable, and delete symmetric keys
    * **Customer Managed Keys** 
    * **Data Keys**
    * **Envelope Encryption**
    * **Encryption Context**
  * **CloudHSM**
    * A service providing you with secure cryptographic key storage by making Hardware Security Modules \(HSMs\) available on the AWS cloud
  * **AWS CloudTrail**
    * provides visibility into user activity by recording API calls made on your account
* Analytics
  * **Amazon Kinesis**
    * **Amazon Kinesis Firehose:** A service enabling you to load massive volumes of streaming data into AWS
    * **Amazon Kinesis Streams:** A service enabling you to build custom applications for more complex analysis of streaming data in real time
    * **Amazon Kinesis Analytics:** A service enabling you to easily analyze streaming data real time with standard SQL
  * **Amazon Elastic MapReduce \(Amazon EMR\)**
    * **Hadoop Distributed File System \(HDFS\)** 
      * _HDFS_ is the standard file system that comes with Hadoop. All data is replicated across multiple instances to ensure durability. 
    * **EMR File System \(EMRFS\)** 
      * an implementation of HDFS that allows clusters to store data on Amazon S3.
  * **AWS Data Pipeline**
    * _AWS Data Pipeline_ is a web service that helps you reliably process and move data between different AWS compute and storage services, and also on-premises data sources, at specified intervals. 
* DevOps
  * **AWS OpsWorks**
    * a configuration management service that helps you configure and operate applications using Chef. 
  * **AWS CloudFormation**
    * _AWS CloudFormation_ is a service that helps you model and set up your AWS resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS.
  * **AWS Elastic Beanstalk**
    * _AWS Elastic Beanstalk_ is the fastest and simplest way to get an application up and running on AWS. 
  * **AWS Trusted Advisor**
    * _AWS Trusted Advisor_ draws upon best practices learned from the aggregated operational history of serving over a million AWS customers. 
  * **AWS Config**
    * _AWS Config_ is a fully managed service that provides you with an AWS resource inventory, configuration history, and configuration change notifications to enable security and governance. 

