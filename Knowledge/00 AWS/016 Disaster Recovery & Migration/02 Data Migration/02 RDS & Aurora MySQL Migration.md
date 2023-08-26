# RDS MySQL to Aurora MySQL
---

## Option 1
---

* **DB Snapshots** from RDS MySQL **restored as MySQL Aurora DB**

![[Pasted image 20230823191828.png]]

## Option 2
---

* **Create an Aurora Read Replica** from your RDS MySQL, and when the replication lag is 0, **promote it as its own DB cluster** 
	* Can **take time and cost $**

![[Pasted image 20230823191952.png]]


# External MySQL to Aurora MySQL
---

## Option 1
---

* Use Percona XtraBackup to **create a file backup in Amazon S3** 
* **Create an Aurora MySQL DB** from Amazon S3

![[Pasted image 20230823192141.png]]

## Option 2
---

* **Create an Aurora MySQL DB**
* Use the **mysqldump** utility to migrate MySQL into Aurora (**slower than S3 method**)

![[Pasted image 20230823192327.png]]

# DMS
---

*  Use DMS if **both databases are up and running**