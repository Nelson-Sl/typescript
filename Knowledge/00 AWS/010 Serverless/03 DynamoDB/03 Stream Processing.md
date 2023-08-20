# What is Stream Processing in DynamoDB?
---

* **Ordered stream of item-level modifications (create/update/delete)** in a table

# Use Cases
---

* **React to changes in real-time** (welcome email to users) 
* **Real-time usage analytics**
* Insert into **derivative tables** 
* Implement **cross-region replication** 
* **Invoke AWS Lambda on changes** to your DynamoDB table

# vs Kinesis Data Streams (newer)
---

* DynamoDB Streams
	* **24 hours** retention 
	* **Limited # of consumers**
	* Process using **AWS Lambda Triggers**, or **DynamoDB Stream Kinesis adapter**
* Kinesis Data Streams (newer)
	* 1 year retention (Longer)
	* **High # of consumers**
	* Process using **AWS Lambda**, **Kinesis Data Analytics**, **Kineis Data Firehose**, **AWS Glue Streaming ETL**…

![[Pasted image 20230818124437.png]]
