# Chapter 9: DNS&Route 53

**Domain Name System \(DNS\) and Amazon Route 53**

* **Domain Name System \(DNS\)**
  * Basics: DNS is a globally-distributed service that is foundational to the way people use the Internet.
  * For Example: www.amazon .com and aws.amazon.com
    * com is the Top-Level Domain \(TLD\)
    * amazon is the Second-Level Domain \(SLD\)
    * There can be any number of lower levels \(for example, www and aws\) below the SLD.
  * **Top-Level Domains \(TLDs\)**
    * The TLD is the farthest portion to the right \(as separated by a dot\). Common TLDs are .com, .net, .org, .gov, .edu, and .io.
    * Certain parties are given management control over TLDs by the Internet Corporation for Assigned Names and Numbers \(ICANN\).
  * **Fully Qualified Domain Name \(FQDN\)**
    * api.aws.amazon.com. :FQDN
      * api: host
      * aws.amazon.com: sub domain
      * amazonL SLD
      * .com: TLD
      * api.aws.amazon.com: Domain Name
  * Zone File
    * a simple text file that contains the mappings between domain names and IP addresses. \(Hash Tables????\)
* **Steps Involved in Domain Name System \(DNS\) Resolution**
  * When you type a domain name into your browser, your computer first checks its host file to see if it has that domain name stored locally. If it does not, it will check its DNS cache to see if you have visited the site before. If it still does not have a record of that domain name, it will contact a DNS server to resolve the domain name.
  * DNS starts with TLDs \(for example, .com, .edu\). The Internet Assigned Numbers Authority \(IANA\) controls the TLDs in a root zone database, which is essentially a database of all available TLDs.
  * DNS names are registered with a domain registrar. A registrar is an authority that can assign domain names directly under one or more TLDs. These domains are registered with InterNIC, a service of ICANN, which enforces the uniqueness of domain names across the Internet. Each domain name becomes registered in a central database, known as the WhoIS database.
* Record Types
  * A
  * AAAA
  * CNAME
  * MX
  * NS
  * PTR
  * SOA
  * SPF
  * TXT

**Amazon Route 53 Overview**

* **Domain registration**—Amazon Route 53 lets you register domain names, such as example.com.
* **DNS service**—Amazon Route 53 translates friendly domain names like [www.example.com](www.example.com) into IP addresses like 192.0.2.1.
* **Health checking**—Amazon Route 53 sends automated requests over the Internet to your application to verify that it’s reachable, available, and functional.

Amazon Route 53 allows you to have several different routing policies, including the following:

**Simple**—Most commonly used when you have a single resource that performs a given function for your domain

**Weighted**—Used when you want to route a percentage of your traffic to one particular resource or resources

**Latency-Based**—Used to route your traffic based on the lowest latency so that your

users get the fastest response times

**Failover**—Used for DR and to route your traffic from your resources in a primary location to a standby location

**Geolocation**—Used to route your traffic based on your end user’s location

