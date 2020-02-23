# Chapter 7: Databases and AWS

\*\*\*\*

\*\*\*\*

_Note:_ A strong understanding of essential database concepts, Amazon RDS, and Amazon DynamoDB are required to pass this exam.

* **Relational Databases**
  * relational database can be categorized as either an _Online Transaction Processing \(OLTP\)_ or _Online Analytical Processing \(OLAP\)_ database system
* **Data Warehouses**
  * A _data warehouse_ is a central repository for data that can come from one or more sources.
  * This data repository is often a specialized type of relational database that can be used for reporting and analysis via OLAP. 
* **NoSQL Databases**
  * A common use case for NoSQL is managing user session state, user profiles, shopping cart data, or time-series data.
* **Amazon Relational Database Service \(Amazon RDS\)**
  * Amazon RDS exposes a database endpoint to which client software can connect and execute SQL.
  * **Storage Options**
    * **Magnetic**,also called standard storage,
    * **General Purpose \(SSD\)**
    * **Provisioned IOPS \(SSD\)** 
  * **Backup and Recovery**
    * _Recovery Point Objective \(RPO\)_
    * _Recovery Time Objective \(RTO\)_
  * **High Availability with Multi-AZ**
    * When you create a Multi-AZ DB Instance, a primary instance is created in one Availability Zone
  * **Scaling Up and Out**
    * Storage expansion is supported for all of the database engines except for SQL Server.
  * **Security**
    * deploy your Amazon RDS DB Instances into a private subnet within an Amazon Virtual Private Cloud \(Amazon VPC\)
    * Protect access to your infrastructure resources using AWS Identity and Access Management \(IAM\) policies
* **Amazon Redshift**

  -- Basics: Amazon Redshift is a relational database designed for OLAP scenarios and optimized for high-performance analysis and reporting of very large datasets.

  * **Clusters and Nodes**
    * _cluster_ -A cluster is composed of a leader node and one or more compute nodes.Each cluster contains one or more databases. 
  * **Table Design**
  * **Compression Encoding**
  * **Distribution Strategy**
  * **Loading Data**
  * **Querying Data**
  * **Snapshots**
  * **Security**

* **Amazon DynamoDB**

  -- Basics: _Amazon DynamoDB_ is a fully managed NoSQL database service that provides fast and low- latency performance that scales with ease.

  * **Data Model**
  * **Security**
    * IAM 
  * **Streams**
    * To build an application that reads from a shard, it is recommended to use the Amazon DynamoDB Streams Kinesis Adapter. T

