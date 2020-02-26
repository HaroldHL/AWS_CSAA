# Chapter 10: ElastiCache

* In-Memory Caching
  * Round-trips back and forth to a database and its underlying storage can add significant delays and are often the top contributor to application latency.
  * Caching frequently-used data is one of the most important performance optimizations you can make in your applications.
  * **Redis** is a flexible in-memory data structure store that can be used as a cache, database, or even as a message broker. 
* **Amazon ElastiCache**
  * You can use Amazon ElastiCache in your applications to speed the deployment of cache clusters and reduce the administration required for a distributed cache environment.
  * you can implement any number of caching patterns.
  * **Data Access Patterns**
    * Retrieving a flat key from an in-memory cache 
  * **Cache Engines**
    * **Memcached**
      * allows you to write and read objects into in-memory key/value data store
      * elastically grow and shrink a cluster of Memcached nodes to meet your demands
    * **Redis**
      * Unlike Memcached, Redis supports the ability to persist the in-memory data onto disk. create snapshots that back up your data and then recover or replicate from the backups.
      * It's easy to sort and rank data
  * **Nodes and Clusters**
    * A single Memcached cluster can contain up to 20 nodes
    * Redis clusters are always made up of a single node; however, multiple clusters can be grouped into a _Redis replication group_.
  * **Replication and Multi-AZ**
    * Cache clusters running Redis support the concept of _replication groups_. A replication group consists of up to six clusters, with five of them designated as read replicas. 
    * Amazon ElastiCache clusters running Redis support **both of these design requirements**. Unlike Redis, cache clusters running Memcached are standalone in-memory services without any redundant data protection services.
    * In the event the primary node fails or can’t be reached, Multi-AZ will select and promote a read replica to become the new primary, and a new node will be provisioned to replace the failed one. 
  * **Backup and Recovery**
    * running Redis allow you to persist your data from in-memory to disk and create a _snapshot_
    * Snapshots cannot be created for clusters using the Memcached engine because it is a purely in-memory key/value store and always starts empty
  * **Access Control**
    * is controlled primarily by restricting inbound network access to your cluster.
    * When deployed inside of a Virtual Private Cloud \(VPC\), each node will be issued a private IP address within one or more subnets that you select.
    * Using the AWS Identity and Access Management \(IAM\) service, you can define policies that control which AWS users can manage the Amazon ElastiCache infrastructure itself.

