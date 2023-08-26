# RDS PostgreSQL to Aurora PostgreSQL
---

## Option 1
---

* **DB Snapshots** from RDS PostgreSQL **restored as PostgreSQL Aurora DB**

![[Pasted image 20230823192554.png]]

## Option 2
---

* **Create an Aurora Read Replica** from your RDS PostgreSQL, and when the replication lag is 0, **promote it as its own DB cluster** 
	* Can **take time and cost $**

![[Pasted image 20230823192646.png]]



# External MySQL to Aurora MySQL
---

* Create a backup and put it in Amazon S3
* Import it using the **aws_s3 Aurora extension**

![[Pasted image 20230823192837.png]]

# DMS
---

*  Use DMS if **both databases are up and running**