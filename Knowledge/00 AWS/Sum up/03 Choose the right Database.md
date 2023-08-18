# RDBMS (= SQL / OLTP)
---

* RDS, Aurora
	* Store **relational datasets (RDBMS / OLTP)**, perform **SQL queries, transactions**
		* Great for JOIN Queries
	* Aurora **Cost 20% higher**, but with **less maintenance / more flexibility / more performance / more features**


# NoSQL Database
---

## ElasticCache: Key/Value Pair
---

* **Frequent Read But Less Writes**
	* cache **results for DB queries**
	* **store session data** for websites
* Can't use SQL & Need Application Change

## DynamoDB
---

* Distributed serverless cache
	* Can replace ElastiCache as a key/value store (storing session data for example, using TTL feature), **distributed but slight lower performance**
* Serverless applications development (**small documents** 100s KB)
* Great for application to **rapidly evolve schemas**

## Document DB
---

* AWS version of **MongoDB**, store, query, and index JSON data
	* Fully Managed, **highly available with replication across 3 AZ** (Deployment Similar to Aurora)
	* automatically **grows in increments of 10GB, up to 64 TB**
	* Automatically **scales to workloads with millions of requests per seconds**

## Amazon KeySpaces (For Amazon Cassandra)
---

* an **open-source NoSQL distributed** database
	* **Serverless**
	* **Scalable** (Auto-Scaled based on application's traffic)
	* **highly available** (Tables are replicated 3 times across multiple AZ)
	* Fully managed by AWS
	* Feature
		* Capacity: **On-demand mode** or **provisioned mode with auto-scaling** (Similar to DynamoDB)
		* Encryption, backup, Point-In-Time Recovery (PITR) up to 35 days (Similar to DynamoDB)
	* Performance
		* Single-digit millisecond latency at any scale, **1000s of requests per second**

* Use Case: **Store IoT devices info**, **time-series data**, …
# Object Store: S3 / Glacier
---

* S3
	* store **static files**
	* key value store for **big files**
	* **Media / Website hosting**
	* **Archive Files**
* Glacier
	* **Archive Files**

# Graph Database: AWS Neptune
---

* Fully managed **graph** database, displays **relationships between data**
	* **Highly available across 3 AZ, with up to 15 read replicas, across AZs** (Similar to Aurora)
	* Can **store up to billions of relations and query** the graph with milliseconds latency
* Use Cases
	* Good for build and run applications **working with highly connected datasets** – optimized for these complex and hard queries
		* E.g. **knowledge graphs (Wikipedia)**, **fraud detection**, **recommendation** **engines**, **social networking**

# Ledger: Amazon Quantum Ledger Database (QLDB)
---

* Used to **review history of all the changes made to your application data** over time
	* Immutable system: **no entry can be removed or modified**, cryptographically verifiable
	* Fully Managed, **Serverless**, **High available**, **Replication across 3 AZ**
	* manipulate data using **SQL**
	* 2-3x better performance **than common ledger blockchain frameworks**
* Use Case
	* Good for **Financial Product**

![[Pasted image 20230818182553.png]]

## Vs. Amazon Managed Blockchain
---

* **No decentralization component**, in accordance with financial regulation rules

# Time series: Amazon Timestream
---

* Fully-Managed Database **based on time-series**
	* Scheduled queries, multi-measure records, SQL compatibility
	* fast
		* Store and analyze trillions of events per day & **1000s times faster** & 1/10th the cost of relational databases
	* scalable
		* Automatically scales up/down to adjust capacity
	* serverless
	* Feature
		* Data storage tiering: **recent data kept in memory** and **historical data kept in a cost-optimized storage**
		* **Built-in time series analytics functions** (helps you identify patterns in your data in near real-time)
	* Secure
		* Encryption in transit and at rest

![[Pasted image 20230818183425.png]]

## Use Cases
---

* **IoT apps**, **operational applications**, **real -time analytics**, …