# Definition
---

Aurora is a **propritetary** database that developed by AWS, which supports **PostgreSQL** and **AuroraDB**

![[Pasted image 20230806174331.png]]

# Features
---

## High Availability & Auto Failover
---

* There will be 6 copies for your data across 3 Availability Zones. **4** out of 6 is required for **read** and **3** out of 6 is required for **write**. The storage is striped across **100s** of volumes
* **One Master Instance** will takes the read task, and Master + up

![[Pasted image 20230806175159.png]]


# Pros & Cons
---

* Pros
	* Higher Avaliability & Read Scaling
		* Can have up to 15 [[03 Read Replicas|read replicas]] and the replication process is **faster than MySQL**
		* Aurora is **HA native** and the failover is **instantaneous**
	* Higher Performance
		* **3x performance** improvement than PostgreSQL on RDS
		* **5x performance** improvement than MySQL on RDS
* Cons