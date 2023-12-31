# What's MSK?
---

* An alternative to Amazon Kinesis & Fully managed Apache Kafka on AWS 
	* Allow you to **create, update, delete** clusters 
	* MSK creates & manages Kafka brokers nodes & Zookeeper nodes for you
	* Deploy the MSK cluster in your VPC, **multi-AZ (up to 3 for HA)** 
	* Automatic recovery from common Apache Kafka failures 
	* Data is stored on EBS volumes for as long as you want

![[Pasted image 20230819161025.png]]

# Alternative: MSK Serverless
---

* Run Apache Kafka on MSK **without managing the capacity**
* MSK **automatically provisions resources** and **scales compute & storage**

# Consumers
---

![[Pasted image 20230819161252.png]]

# vs. [[02 Kinesis Data Streams|Kinesis Stream]]
---

* **Higher possible message size limit**

![[Pasted image 20230819161437.png]]