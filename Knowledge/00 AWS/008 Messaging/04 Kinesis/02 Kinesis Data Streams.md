# How Kinesis Data Streams Work?
---

* Producers: **AWS SDK**, **Kinesis Producer Library (KPL)**, **Kinesis Agent**
* Consumers:
	* Write your own: **Kinesis Client Library (KCL)**, **AWS SDK**
	* Managed: **AWS Lambda**, **Kinesis Data Firehose**, **Kinesis Data Analytics**
* Capacity Modes
	* Provision Mode
		* **choose the number of shards provisioned**, scale manually or using API
		*  **1MB/s in** (or 1000 records per second) & **2MB/s out** (classic or enhanced fan-out consumer)
		* pay **per shard provisioned per hour**
	* On-demand mode
		* 

![[Pasted image 20230816221554.png]]
