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

* 