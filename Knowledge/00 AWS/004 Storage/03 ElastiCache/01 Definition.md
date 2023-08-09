# What is ElastiCache?
---

* ElastiCache is a service managed by AWS to **get managed for cache databases** like Redis & Memcached, which provides **high performance** with **low latency**.
	* AWS takes of **setup**, **configuration**, **optimizations**, **monitoring**, **OS maintenance / patching**, **failure recovery & backups**

# How ElastiCache works?
---

![[Pasted image 20230809175216.png]]

# Solution Architecture
---

## DB Cache
---
* Applications **queries ElastiCache**, if notavailable, **get from RDS and store in ElastiCache**. (Must have an **invalidation strategy** or **'write through'** to make sure the most current data is used)
* Benefit: **Help to relieve load in databases**
* Example: **Gaming Leaderboard**

![[Pasted image 20230809175736.png]]

## User Session Store
---

* Save **users' login data in ElastiCache** so that users can retrieve the data and keep logged in (**Using TTL(Time-to-Live) Features**)

![[Pasted image 20230809180005.png]]

# Security For ElasticCache
---

* AWS API-Level Security: **IAM Policy & Authentication**
* Database Level Security
	* Redis
		* First Level: **AWS Security Group**
		* Second Level: **Password / Token** 
		* Support **SSL** In-Flight Encryption
	* Memcached
		* Support **SASL-based** authentication

![[Pasted image 20230809180604.png]]

# Pros & Cons
---
