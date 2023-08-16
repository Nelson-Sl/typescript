# What's queue?
---

![[Pasted image 20230816200547.png]]

# How does SQS Work?
---

## Standard Queue
---

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
	* 
	* Can **have out of order messages** (best effort ordering)

![[Pasted image 20230816202510.png]]

![[Pasted image 20230816202809.png]]
