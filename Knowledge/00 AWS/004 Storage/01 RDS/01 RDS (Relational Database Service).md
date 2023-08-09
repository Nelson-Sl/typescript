# What is RDS?
---

* RDS (Relational Database Service) is a **AWS managed database service** that allows you to create database that **could be queried by SQL language** online.  Some of the examples might be:
	* Postgres
	* MySQL
	* MariaDB
	* Microsoft SQL Server
	* Oracle
	* [[00 AWS/004 Storage/02 Aurora/01 Definition|Aurora (AWS Proptrietary Database)]]

# Can Do & Can't Do
---

* Can
	* Automated provisioning, OS patching 
	* Continuous backups and restore to specific timestamp (Point in Time Restore)! 
	* Monitoring dashboards 
	* [[03 Read Replicas#Improve Read Performance & Run Workload in another application|Read replicas for improved read performance]]
	* [[03 Read Replicas#RDS Multi-AZ (Disaster Recovery)|Multi AZ setup for DR(Disaster Recovery)]]
	* Maintenance windows for upgrades 
	* [[02 Storage Auto Scaling|Scaling capability (vertical and horizontal)]]
	* Storage backed by EBS (gp2 or io1)
* Can't
	* Use **SSH** to enter into instance

# Customization Option
---

This is enabled only in **Oracle** and **Microsoft SQL Server** Database, which provides full admin access to the underlying OS and database, so that you can:
* Configure settings
* Install Patching
* Enable **native features**
* Access the underlying instance using **SSH** or **SSM Session Manager**