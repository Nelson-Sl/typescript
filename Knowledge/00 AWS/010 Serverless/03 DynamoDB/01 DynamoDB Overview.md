# What's DynamoDB?
---

* An AWS managed, **NoSQL database** with **transaction support**
	* Has **Standard** & **Infrequent Access (IA)** Table Class
	* **Integrated with IAM** for security, authorization and administration

## Benefits
---

* **highly available** with **replication across multiple AZs**
* **Low cost** and **auto-scaling** capabilities
* **Fast and consistent in performance** (single-digit millisecond)
	* Scales to massive workloads, distributed database
	* Millions of requests per seconds, trillions of row, 100s of TB of storage
* Good for **frequently evolve schema**

# How DynamoDB Works?
---

## Data Structure
---

* DynamoDB is made of **Tables**
* Each table **has a Primary Key** (must be decided at creation time)
* Each table can **have an infinite number of items (= rows)**
* Each item **has attributes (can be added over time – can be null)** -> Max size of Items is **400KB**

![[Pasted image 20230818120227.png]]

## Support Data Format
---

* **Scalar Types** – String, Number, Binary, Boolean, Null
* **Document Types** – List, Map
* **Set Types** – String Set, Number Set, Binary Set

# Capacity Mode
---
## Provisioned Mode (Default)
---

* Need to **plan capacity beforehand** & **specify the number of reads/writes per second**
* Pay for **provisioned Read Capacity Units (RCU) & Write Capacity Units (WCU)**
* Possibility to **add auto-scaling mode** for RCU & WCU

## On-Demand Mode
---

* **Read/writes automatically scale up/down with your workloads** & No capacity planning needed
* Pay for what you use, **more expensive**
* Great for **unpredictable workloads, steep sudden spikes**

# Features
---

* [[02 DynamoDB Accelerator (DAX)|DynamoDB Accelerator (DAX)]]: Fast DynamoDB Cache Tool
* [[03 Stream Processing|Dynamo DB Stream Processing]]
* [[04 DynamoDB Global Table|DynamoDB Global Table]]: Read / Write Dynamo DB Table across region
* [[05 Time to Live (TTL)|Dynamo DB TTL]]: Automatically Delete DB Items at a specific time

# Backups
---

* Continuous backups using **point-in-time recovery (PITR)**
	* Optionally enabled **for the last 35 days**
	* Point-in-time recovery to **any time within the backup window**
	* The recovery process **creates a new table**
* On-demand backups
	* **Full backups for long-term retention**, until explicitely deleted
	* Doesn’t **affect performance or latency**
	* **Can be configured and managed in AWS Backup** (enables **cross-region copy**)
	* The recovery process **creates a new table**

# Integration
---

## Import From S3
---

* **Creates a new table** & Doesn’t **consume any write capacity**
* Import errors **are logged in CloudWatch Logs**

![[Pasted image 20230818130739.png]]

## Export to S3
---

* Works for any point of time **in the last 35 days** (Must Enable **Point-in-Time Recovery**)
* Doesn’t affect the read capacity of your table
* Export in DynamoDB JSON or ION format

![[Pasted image 20230818131142.png]]

### Use Cases
---

* Perform **data analysis** on top of DynamoDB (Athena)
* **Retain snapshots** for auditing
* **ETL on top of S3 data** before importing back into DynamoDB