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
		* No need to provision or manage the capacity, **scales automatically based on observed throughput peak during the last 30 days**
		* Default capacity provisioned (**4 MB/s in or 4000 records per second**)
		* Pay **per stream per hour & data in/out per GB**
* Note: Data that **shares the same partition goes to the same shard** (ordering)
	* Advantage: Good for data transfer if you **have < 5 consumers** and need to **transfer large data for each consumer in time**

![[Pasted image 20230816221554.png]]

# Features
---

* Data Retention **between 1 day to 365 days**
* Ability to **reprocess (replay) data**
* Immutability: Once data is inserted in Kinesis, **it can’t be deleted**

# Security
---

* Access Controls
	* Account Level: **IAM policies** to regulate access 
* Encryption
	* In-flight: **HTTPS API**
	* At-Rest: **KMS Keys**
	* **Client-side encryption** if the client wants to perform encryption/decryption itself (But it's harder)
* Request Security
	* **VPC Endpoints available for Kinesis** to access within VPC
	* Monitor API calls using **CloudTrail**
