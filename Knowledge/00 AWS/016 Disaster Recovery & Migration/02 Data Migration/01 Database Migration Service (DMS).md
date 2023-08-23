# What's Database Migration Service (DMS)?
---

* Quickly and securely **migrate databases to AWS**, **resilient**, **self healing**
	* The source database **remains available during the migration**
	* You must **create an EC2 instance** to perform the replication tasks
	* Supports:
		* **Homogeneous** migrations (E.g. **Oracle to Oracle**)
		* **Heterogeneous** migrations (E.g. **Microsoft SQL Server to Aurora**)

![[Pasted image 20230823185913.png]]

# DMS Sources & Targets
---

## Sources
---

* On-Premises and EC2 instances databases: **Oracle, MS SQL Server, MySQL, MariaDB, PostgreSQL, MongoDB, SAP, DB2** 
* Azure: **Azure SQL Database** 
* **Amazon RDS**: all including Aurora 
* **Amazon S3** 
* **DocumentDB**

## Targets
---

* On-Premises and EC2 instances databases: **Oracle, MS SQL Server, MySQL, MariaDB, PostgreSQL, SAP** 
* Amazon **RDS** 
* **Redshift, DynamoDB, S3** 
* **OpenSearch** Service 
* **Kinesis Data Streams** 
* **Apache Kafka** 
* **DocumentDB & Amazon Neptune** 
* **Redis & Babelfish**

# Feature
---

## AWS Schema Conversion Tool (SCT)
---

* Convert your Database’s Schema **from one engine to another**
	* E.g. 
		* **OLTP**: (SQL Server or Oracle) to MySQL, PostgreSQL, Aurora
		* **OLAP**: (Teradata or Oracle) to Amazon Redshift
	* Prefer **compute-intensive instances** to optimize data conversions

![[Pasted image 20230823190627.png]]

## Continuous Replication (Using CDC)
---

![[Pasted image 20230823190746.png]]

## Multi-AZ Deployment
---

* When Multi-AZ Enabled, DMS **provisions and maintains a synchronously stand replica in a different AZ**
	* Advantages: Provides **Data Redundancy**, Eliminates **I/O freezes**, **Minimizes latency spikes**

![[Pasted image 20230823190905.png]]
