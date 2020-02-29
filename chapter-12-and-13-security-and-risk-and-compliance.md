# Chapter 12&13: Security& Risk and Compliance



**Security**

* Security Model\*\*

  The shared responsibility model is the security model where AWS is responsible for the security of the underlying cloud infrastructure, and the customer is responsible for securing workloads deployed in AWS. Customers benefit from a data center and network architecture built to satisfy the requirements of AWS most security-sensitive customers. This means that customers get a resilient infrastructure, designed for high security, without the capital outlay and operational overhead of a traditional data center.

* **Account Level Security**

  AWS credentials help ensure that only authorized users and processes access your AWS account and resources. AWS uses several types of credentials for authentication. These include passwords, cryptographic keys, digital signatures, and certificates. AWS also provides the option of requiring MFA to log in to your AWS account or IAM user accounts.

  Passwords are required to access your AWS account, individual IAM user accounts, AWS Discussion Forums, and the AWS Support Center. You specify the password when you first create the account, and you can change it at any time by going to the Security Credentials page.

  **AWS MFA** is an additional layer of security for accessing AWS Cloud services. When you enable this optional feature, you will need to provide a six-digit, single-use code in addition to your standard user name and password credentials before access is granted to your AWS account settings or AWS Cloud services and resources. You get this single-use code from an authentication device that you keep in your physical possession. This is multi-factor because more than one authentication factor is checked before access is granted: a password \(something you know\) and the precise code from your authentication device \(something you have\). An MFA device uses a software application that generates six-digit authentication codes that are compatible with the TOTP standard, as described in RFC 6238.

  Access Keys are created by **AWS IAM** and delivered as a pair: the Access Key ID \(AKI\) and the Secret Access Key \(SAK\). AWS requires that all API requests be signed by the SAK; that is, they must include a digital signature that AWS can use to verify the identity of the requestor. You calculate the digital signature using a cryptographic hash function. If you use any of the AWS SDKs to generate requests, the digital signature calculation is done for you. The most recent version of the digital signature calculation process at the time of this writing is Signature Version 4, which calculates the signature using the HMAC-SHA-256 protocol.

  **AWS CloudTrail** is a web service that records API calls made on your account and delivers log files to your Amazon S3 bucket. AWS CloudTrail’s benefit is visibility into account activity by recording API calls made on your account.

* **Service-Specific Security**
  * **Compute**
    * **Amazon Elastic Compute Cloud \(Amazon EC2\)** 
      * RSA 2048 SSH-2 Key pairs for gaining first access to an Amazon EC2 instance.
      * On a Linux instance, access is granted through showing possession of the SSH private key
      * On a Windows instance, SSH private key in order to decrypt the administrator password.
  * **Networking**
    * **Elastic Load Balancing**
    * **Amazon Virtual Private Cloud \(Amazon VPC\)** 
    * **Amazon CloudFront** 
  * **Storage**
    * **Amazon Simple Storage Service \(Amazon S3\)**
    * **Amazon Glacier**
    * **AWS Storage Gateway**
  * **Database**
    * **Amazon DynamoDB** 
    * **Amazon Relational Database Service \(RDS\)** 
    * **Amazon Redshift**
  * **Application Services**
    * **Amazon Simple Queue Service \(SQS\)**
    * **Amazon Simple Notification Service \(SNS\)**
  * **Analytics**
    * **Amazon Elastic MapReduce \(Amazon EMR\)**
    * **Amazon Kinesis**
  * **Deployment and Management**
    * **AWS Identity and Access Management \(IAM\)**
  * **Mobile Services**
    * **Amazon Cognito**

      Amazon Cognito provides identity and sync services for mobile and web- based applications. Your application authenticates with one of the well-known identity providers such as Google, Facebook, and Amazon using the provider’s SDK. After the end user is authenticated with the provider, an OAuth or OpenID Connect token returned from

      the provider is passed by your application to Amazon Cognito, which returns a new Amazon Cognito ID for the user and a set of temporary, limited-privilege AWS credentials.
  * **Applications**
    * **Amazon Workspaces**

**Risk and Compliance**

AWS communicates with customers regarding its security and control environment through the following mechanisms:

* Obtaining industry certifications and independent third-party attestations
* Publishing information about security and AWS control practices via the website, whitepapers, and blogs
* Directly providing customers with certificates, reports, and other documentation \(under NDA in some cases\)

AWS has achieved a number of internationally recognized certifications and accreditations that demonstrate AWS compliance with third-party assurance frameworks, including:

* FedRAMP
* FIPS 140–2
* FISMA and DIACAP
* HIPAA
* ISO 9001
* ISO 27001
* ITAR
* PCI DSS Level 1
* SOC 1/ISAE 3402
* SOC 2
* SOC 3

