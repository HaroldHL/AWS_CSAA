# Chapter 6: IAM

**AWS Identity and Access Management \(IAM\)**

--The first IAM concept to understand is principals

Three types of principals:

* root users
  * begin with only a single sign-in principal that has complete access to all AWS Cloud services and resources in the account. Called Root Users
* IAM users
  * You may create separate IAM users for each member of your operations team so they can interact with the console and use the CLI
* roles/temporary security tokens
  * When one of these actors assumes a role, AWS provides the actor with a temporary security token from the _AWS Security Token Service \(STS\)_ that the actor can use to access AWS Cloud services
  * Roles and temporary security tokens enable a number of use cases:
    * **Amazon EC2 Roles**
      * Using IAM roles for Amazon EC2 removes the need to store AWS credentials in a configuration file.
    * **Cross-Account Access**
      * This is highly recommended as a best practice, as opposed to distributing access keys outside your organization.
    * **Federation**
      * _IAM Identity Providers_ provide the ability to federate these outside identities with IAM and assign privileges to those users authenticated outside of IAM.

| Princial | Traits |
| :--- | :--- |
| Root Users |  |
| IAM Users | Access controlled by policy  Durable  Can be removed by IAM administrator |
| Roles/Temporary Security Tokens | Access controlled by policy Temporary Expire after specific time interval |

**Authentication**

* **User Name/Password**
* **Access Key**
* **Access Key/Session Token**

_Note_: It is important to note that when an IAM user is created, it has neither an access key nor a password, and the IAM administrator can set up either or both.

**Authorization**

Authorization is handled in IAM by defining specific privileges in _policies_ and associating those policies with principals.

**Policies**

* _Effect_ -A single word: Allow or Deny.
* _Service_ - what service does this permission apply?
* _Resource_ - The resource value specifies the specific AWS infrastructure for which this permission applies. Basic Fomat:"arn:aws:service:region:account-id:\[resourcetype:\]resource"
* _Action_ - The action value specifies the subset of actions within a **service** that the permission allows or denies. 
* **Condition**

**Associating Policies with Principals**

* **User Policy**
* **Managed Policies**
* **Group Policy**
* **Managed Policies**

_NOTE_:A good first step is to use the root user to create a new IAM group called “IAM Administrators” and assign the managed policy, “IAMFullAccess.” Then create a new IAM user called “Administrator,” assign a password, and add it to the IAM Administrators group. At this point, you can log off as the root user and perform all further administration with the IAM user account.

**Other Key Features**

* **Multi-Factor Authentication \(MFA\)**
  * With MFA, authentication also requires entering a One-Time Password \(OTP\) from a small device.
* **Rotating Keys**
  * Access keys should be rotated on a regular schedule.

**Summary**

IAM is a powerful service that gives you the ability to control which people and applications can access your AWS account at a very granular level. Because the root user in an AWS account cannot be limited, you should set up IAM users and temporary security tokens for your people and processes to interact with AWS.

Policies define what actions can and cannot be taken. Policies are associated with IAM users either directly or through group membership. A temporary security token is associated with a policy by assuming an IAM role. You can write your own policies or use one of the managed policies provided by AWS.

Common use cases for IAM roles include federating identities from external IdPs, assigning privileges to an Amazon EC2 instance where they can be assumed by applications running on the instance, and cross-account access.

IAM user accounts can be further secured by rotating keys, implementing MFA, and adding conditions to policies. MFA ensures that authentication is based on something you have in addition to something you know, and conditions can add further restrictions such as limiting client IP address ranges or setting a particular time interval.

