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

# SNS Limits
---

* **100,000 topics limit** (Can be adjusted)
* **Up to 12,500,000 subscriptions** per topic

# SNS Security
---

*  Access Controls
	* Account Level: **IAM policies** to regulate access to the SQS API
	* SQS Access Policies (similar to S3 bucket policies)
		* Cross-account access to SQS queues
		* Allowing other services (**SNS, S3…**) to write to an SQS queue
* Encryption
	* In-flight: **HTTPS API**
	* At-Rest: **KMS Keys** Or **SQS Keys**
	* **Client-side encryption** if the client wants to perform encryption/decryption itself