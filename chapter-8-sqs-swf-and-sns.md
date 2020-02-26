# Chapter 8: SQS, SWF, and SNS

* **Amazon Simple Queue Service \(Amazon SQS\)**

  Basics: mazon SQS is a fast, reliable, scalable, and fully managed message queuing service.

  An _Amazon SQS queue_ is basically a buffer between the application components that receive data and those components that process the data in your system.

* **Message Lifecycle**
  * Component 1 sends Message A to a queue, and the message is redundantly distributed

    across the Amazon SQS servers.

  * When Component 2 is ready to process a message, it retrieves messages from the queue, and Message A is returned. While Message A is being processed, it remains in the queue and is not returned to subsequently receive requests for the duration of the visibility timeout.
  * Component 2 deletes Message A from the queue to prevent the message from being received and processed again after the visibility timeout expires.
* **Queue Operations, Unique IDs, and Metadata**
  * CreateQueue
  * ListQueues
  * DeleteQueue
  * SendMessage
  * SendMessageBatch
  * ReceiveMessage
  * ...
  * Your messages are identified via a globally **unique ID** that Amazon SQS returns when the message is delivered to the queue.
* **Queue and Message Identifiers**
  * queue URLs
  * message IDs
  * receipt handles

**Amazon Simple Notification Service \(Amazon SNS\)**

 Basics：Amazon SNS is a web service for mobile and enterprise messaging that enables you to set up, operate, and send notifications.

Amazon SNS follows the publish-subscribe \(pub-sub\) messaging paradigm

* **Common Amazon SNS Scenarios**
  * **Fanout**
    * A fanout scenario is when an Amazon SNS message is sent to a topic and then replicated and pushed to multiple Amazon SQS queues, HTTP endpoints, or email addresses
  * **Application and System Alerts**
  * **Push Email and Text Messaging**
  * **Mobile Push Notifications**

