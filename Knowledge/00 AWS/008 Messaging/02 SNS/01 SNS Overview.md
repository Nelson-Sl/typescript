# What's SNS 
---

* Simple Notification Service (SNS) is an AWS Service **that applies Publisher/Subscriber model to send message**

![[Pasted image 20230816211913.png]]

# How SNS Works?
---

* The “event producer” only **sends message to one SNS topic**
	* Topic Publish (for **SDK**): **Create a topic** -> **Create a subscription (or many)** -> **Publish to the topic**
	* Direct Publish (for **Mobile App SDK**): Create a **platform application** -> Create a **platform endpoint** -> **Publish to the platform endpoint**
		* Works with **Google GCM, Apple APNS, Amazon ADM**…
* As **many “event receivers” (subscriptions) as we want to listen to the SNS topic notifications**
* Each subscriber to the topic **will get all the messages** (note: new feature to filter messages)

![[Pasted image 20230816212312.png]]

![[Pasted image 20230816212227.png]]

## FIFO For Subscribers
---

* **Ordering by Message Group ID** (all messages in the same group are ordered)
* **Deduplication** using a Deduplication ID or Content Based Deduplication
* Limited throughput (same throughput as [[01 SQS#FIFO Queues|SQS FIFO]])

![[Pasted image 20230816214134.png]]
# SNS Limits
---

* **100,000 topics limit** (Can be adjusted)
* **Up to 12,500,000 subscriptions** per topic

# SNS Features: Message Filtering
---

* JSON policy used to **filter messages sent to SNS topic’s subscriptions** (By default it receives every message)

![[Pasted image 20230816213931.png]]

# SNS Security
---

*  Access Controls
	* Account Level: **IAM policies** to regulate access to the SNS API
	* SQS Access Policies (similar to S3 bucket policies)
		* Cross-account access to SQS queues
		* Allowing other services (**SQS, S3…**) to write to an SNS Topic
* Encryption
	* In-flight: **HTTPS API**
	* At-Rest: **KMS Keys**
	* **Client-side encryption** if the client wants to perform encryption/decryption itself