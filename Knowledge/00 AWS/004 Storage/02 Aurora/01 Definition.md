# Definition
---

Aurora is a **propritetary** database that developed by AWS, which supports **PostgreSQL** and **AuroraDB**

![[Pasted image 20230806174331.png]]

# Features
---

## High Availability & Auto Failover
---

* There will be 6 copies for your data across 3 Availability Zones. **4** out of 6 is required for **read** and **3** out of 6 is required for **write**. The storage is striped across **100s** of volumes
* **One Master Instance** will takes the write task, and **Master + up to 15 read replicas** will take the read task
	* Support **Cross-Region** Replication
	* **Self-healing** with peer-to-peer replication
* Automation failover in master will be finished at **less than 30 seconds**

![[Pasted image 20230806175159.png]]

## Auto Scaling
---

* Aurora can be scaled from **10GB** to **128TB**

![[Pasted image 20230806222221.png]]

## Custom Endpoint
---

* Define **a subset of Aurora Instances** as a Custom Endpoint ( After defining this **reader endpoint is generally not used** )
* E.g. Run Example Queries **on specific instances**

![[Pasted image 20230806222924.png]]

## Aurora Serverless
---

* **Automated database initialization** & **Auto-Scaling** based on actual usage ( Therefore **capacity planning needed** )
* **Pay per second**, can be more cost-effective
* E.g. Good for **infrequent, intermittent or unpredictable** workloads

![[Pasted image 20230806224434.png]]

## Aurora Multi-Master
---

* Provide **continuous write availability** for the writer nodes
* Every node does **Read / Write** vs Promote a **Read Replica** as the new master

![[Pasted image 20230806225240.png]]

# Global Aurora
---

* Aurora Cross Region Read Replicas: Can be useful for **disaster recovery** & Simple to **put in place**
* Aurora **Global Database** (recommended)
	* 1 Primary Region ( **Read / Write** )
	* Up to **5 secondary (read-only) regions**, replication lag is less than 1 second
	* Up to **16 Read Replicas** per secondary region ( Help for **decreasing latency** )
* Performance
	* **Cross-region Replication** **<** 1 sec
	* **Promoting another region (for disaster recovery)** **<** 1 min

![[Pasted image 20230806232634.png]]

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
	* **20%** more expensive with RDS (But more efficient)