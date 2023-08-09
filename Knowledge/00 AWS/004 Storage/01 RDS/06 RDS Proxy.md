# What is RDS Proxy
---

* It's a **database proxy** fully managed by AWS and designed for RDS, which allows apps to **pool and share DB connections established with database**.
	* Supports **RDS** ( **MySQL**, **PostgreSQL**, **MariaDB**, **MS SQL Server** ) and **Aurora** ( **MySQL**, **PostgreSQL** )

# How RDS Proxy Works?
---

* Not publicly assessible and should be accessed through **VPC**
* Enforce **IAM Authentication for DB**, and securely **store credentials in AWS Secrets Manager**

![[Pasted image 20230809115607.png]]

# Why use RDS Proxy
---

* Improving database efficiency by **reducing the stress on database resources** (e.g., CPU, RAM) and **minimize open connections** (and timeouts)
* Serverless, autoscaling, highly available (multi-AZ)
* Reduced RDS & Aurora failover time by up **66%**