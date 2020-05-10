# Chapter 1&2: AWS & S3



**Chapter 1**

**Introduction to AWS**

* **Cloud Computing?**

  ----_Cloud computing_ is the on-demand delivery of IT resources and applications via the Internet with pay-as-you-go pricing.

* **6 Advantages of Cloud Computing**
  * **Variable vs. Capital Expense**
  * **Economies of Scale**
  * **Stop Guessing Capacity**
  * **Increase Speed and Agility**
  * **Focus on Business Differentiators**
  * **Go Global in Minutes**
* **Cloud Computing Deployment Models**
  * “all-in” cloud-based deployments
  * hybrid deployments\(on-premises infrastructure&cloud services\)
* **AWS Fundamentals**

  -- AWS provides a highly available technology infrastructures platform with multiple locations worldwide. These locations are composed of regions and vailability Zones.

  * Global Infrastructure
  * Security and Compliance

* **Different Types of AWS services**
  * **Compute and Networking Services**
    * EC2
    * Lambda
    * Auto Scaling
    * Elastic Load Balancing
    * AWS Elastic Beanstalk
    * VPC
    * Direct Connect
    * Route 53 =DNS web service
  * **Storage and Content Delivery**
    * **S3**
    * Amazon Glacier
    * EBS
    * AWS Storage Gateway
    * Amazon CloudFront \(CDN\)
  * **Database Services**
    * Amazon RDS
    * DynamoDB
    * Amazon Redshift  = DB warehouse
    * Amazon ElastiCach
  * **Management Tools**
    * CloudWatch
    * CloudFormation
    * CloudTrail
    * Config
  * **Security and Identity**
    * IAM
    * AWS Key Management Service \(KMS\)
    * AWS Directory Service
    * AWS Certificate Manager
    * AWS Web Application Firewall \(WAF\)
  * **Application Services**

    * API Gateway
    * Elastic Transcoder
    * Simple Notification Service \(Amazon SNS\)
    * Simple Email Service \(Amazon SES\)
    * Simple Workflow Service \(Amazon SWF\)
    * Simple Queue Service \(Amazon SQS\) =message queuing service

    ​

**Chapter 2**

**Amazon S3** & **Amazon Glacier Storage**

S3

---Amazon S3 is cloud **object storage**/Amazon S3 storage is independent of a server and is accessed over the Internet.

Amazon S3 storage common uses cases

* Backup and archive for on-premises or cloud data
* Content, media, and software storage and distribution
* Big data analytics
* Static website hosting
* Cloud-native mobile and Internet application hosting
* Disaster recovery

Traditional IT environments

* _block storage_ \(lower\)
* _file storage_

**S3 Basics**

* **Buckets**
  * A _bucket_ is a container \(web folder\) for objects \(files\) 
  * bucket names are global.
  * create and use multiple buckets/up to 100 per account by default.
* **AWS Regions**
  * each Amazon S3 bucket is created in a specific region that you choose.
* **Objects**
  * Objects can range in size from 0 bytes up to **5TB**
* **Keys**
  * An S3 bucket is identified by a unique identifier called a _key_.
* **Object URL**
  * ​    [http://mybucket.s3.amazonaws.com/fee/fi/fo/fum/jack.docbucket](http://mybucket.s3.amazonaws.com/fee/fi/fo/fum/jack.docbucket) bucket name is still  mybucket, but now the key or filename is the string fee/fi/fo/fum/jack.doc. 
* **Durability and Availability**
  * 99.999999999% durability   _11_
    * store non-critical or easily reproducible derived data \(such as image thumbnails\) - use Reduced Redundancy Storage \(RRS\)
  * 99.99% availability
* **Data Consistency**
  * For PUTs to new objects, this is not a concern—in this case, Amazon S3 provides read-after- write consistency. However, for PUTs to existing objects \(object overwrite to an existing key\) and for object DELETEs, Amazon S3 provides _eventual consistency_.
* **Access Control**
  * Amazon S3 ACLs allow you to grant certain coarse-grained permissions: READ, WRITE, or FULL-CONTROL at the object or bucket level
  * IAM
* **Static Website Hosting**
* **Storage Classes**
  * \*Amazon S3 Standard 
  * _Standard-IA_ – \(Infrequent Access\) 
    * designed for long-lived, less frequently accessed data.Standard-IA has a lower per GB-month storage cost than Standard, but the price model also includes a minimum object size \(128KB\), minimum duration \(30 days\), and per-GB retrieval costs, so it is best suited for infrequently accessed data that is stored for longer than 30 days.
  * _Reduced Redundancy Storage \(RRS\)_ 
    * slightly lower durability
  * _Amazon Glacier_ storage 
    * offers secure, durable, and extremely low-cost cloud storage for data that does not require real-time access, such as archives and long-term backups. 
* **Object Lifecycle Management**
  * Store backup data initially in Amazon S3 Standard.
  * After 30 days, transition to Amazon Standard-IA.
  * After 90 days, transition to Amazon Glacier.
  * After 3 years, delete.
* **Encryption**
  * _SSE-S3 \(AWS-Managed Keys\)_
  * _SSE-KMS \(AWS KMS Keys\)_
    * This is a fully integrated solution where Amazon handles your key management and protection for Amazon S3
  * _SSE-C \(Customer-Provided Keys\)_
  * _Client-Side Encryption_
* **Versioning**
* **MFA Delete**
* **Pre-Signed URLs**
  * the object owner can optionally share objects with others by creating a _pre-signed URL_, using their own security credentials to grant time-limited permission to download the objects
* **Multipart Upload**
  * a three-step process:initiation/uploading the parts/completion
  * you _should_ use multipart upload for objects larger than 100 Mbytes, and you _must_ use multipart upload for objects larger than 5GB
* **Range GETs**
  * only a portion of an object in both Amazon S3 and Amazon Glacier by using something called a _Range_ _GET_
* **Cross-Region Replication**
  * Requirements:
    * versioning must be turned on for both source and destination buckets
    * use an IAM policy to give Amazon S3 permission
  * is commonly used to reduce the latency required to access objects
* **Logging**
* **Event Notifications**

**Amazon Glacier**

--- Amazon Glacier is designed for 99.999999999% durability of objects over a given year.

--- is designed for infrequently accessed data where a retrieval time of three to five hours is acceptable.

* **Archives**
  * data is stored in _archives_
  * All archives are automatically encrypted
  * archives are immutable
* **Vaults**
  * _Vaults_ are containers for archives
  * Each AWS account can have up to 1,000 vaults
* **Vaults Locks**
  * Once locked, the policy can no longer be changed.
* **Data Retrieval**
  * retrieve up to 5% of your data stored in Amazon Glacier for free each month
* **Amazon Glacier versus Amazon Simple Storage Service \(Amazon S3\)**
  * Amazon Glacier supports **40TB** archives _vs_ **5TB** objects in Amazon S3
  * Amazon Glacier are identified by system-generated archive IDs _vs_ S3  “friendly” key names
  * Amazon Glacier archives are automatically encrypted _vs_ S3 optional

