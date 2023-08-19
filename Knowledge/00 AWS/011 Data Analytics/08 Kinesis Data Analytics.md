# What's Kinesis Data Analytics
---

* **Real-time analytics** on Kinesis Data Streams & Firehose using SQL & **can add reference data from Amazon S3** to enrich streaming data
	* Output: 
		* Kinesis Data Streams: **create streams** out of the real-time analytics queries 
		* Kinesis Data Firehose: **send analytics query results** to destinations

![[Pasted image 20230819155814.png]]

# Features & Payment
---

* Features
	* Fully managed, **no servers to provision**
	* Automatic scaling
* Payment
	* Pay for **actual consumption rate**

# Alternative: Kinesis Data Analytics for Apache Flink
---

* **Run any Apache Flink application** on a managed cluster on AWS & Use **Flink (Java, Scala or SQL)** to process and analyze streaming data
	* Support **MSK & Kinesis Data Streams**
	* provisioning compute resources, parallel computation, automatic scaling
	* **application backups** (implemented as checkpoints and snapshots)
	* 

# Use Cases
---

* **Time-series analytics** 
* **Real-time dashboards** 
* **Real-time metrics**