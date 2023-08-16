# What's queue?
---

![[Pasted image 20230816200547.png]]

# How does SQS Work?
---

## Standard Queue
---

* Fully managed service, used to **decouple applications**
### Producing Messages
---

* Produced to SQS **using the SDK (SendMessage API)**
* The message is **persisted in SQS until a consumer deletes it**
* Retention Days: By default **4**, can up to **14 days**
* **Unlimited throughput**, unlimited number of messages in queue
	* E.g. **Order id**

![[Pasted image 20230816202021.png]]

### Consuming Messages
---

* **Poll Message** (up to **10 messages** in a time) -> **Process the messages** (example: insert the message into an RDS database) -> **Delete the messages** using the DeleteMessage API
* With Multiple Customers:
	* Consumers **receive and process messages in parallel**
	* Can have **duplicate messages** (at least once delivery, occasionally)
	* Can **have out of order messages** (best effort ordering)

![[Pasted image 20230816202510.png]]

![[Pasted image 20230816202809.png]]

## FIFO Queues
---
![[Pasted image 20230816205950.png]]

* FIFO = **First In First Out** (ordering of messages in the queue & )
# Features
---

* [[02 Message Visibility Timeout|Message Visibility Timeout]]
# Use Cases
---

## Scaling Horizontally with ASG
---

* Scale EC2 Instances **when message queue length is larger than threshold**

![[Pasted image 20230816203323.png]]

## Decouple between Application Tiers
---

![[Pasted image 20230816203457.png]]

# Security
---

* Access Controls
	* Account Level: **IAM policies** to regulate access to the SQS API
	* SQS Access Policies (similar to S3 bucket policies)
		* Cross-account access to SQS queues
		* Allowing other services (**SNS, S3…**) to write to an SQS queue
* Encryption
	* In-flight: **HTTPS API**
	* At-Rest: **KMS Keys** Or **SQS Keys**
	* **Client-side encryption** if the client wants to perform encryption/decryption itself