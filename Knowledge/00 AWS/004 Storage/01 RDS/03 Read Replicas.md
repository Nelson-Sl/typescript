# About Read Replicas
---

A RDS server could have up to **15 read replicas**, which could within AZ, cross AZ and cross region.
* Replication is **ASYNC**, so reads are eventually consistent
* Replicas can be **promoted to their own DB**
* Applications **must update the connection string** to leverage read replicas
 ![[Pasted image 20230801074616.png]]

# Replica Use Case
---

## Improve Read Performance & Run Workload in another application
---
![[Pasted image 20230801074756.png]]

## RDS Multi-AZ (Disaster Recovery)
---

The database will have a **sync replication** to failover in case of the loss of an AZ, the loss of network, instance & storage failure.
* It **shares the same DNS name** so that it could be an automatic failover to standby
* **No need to manually intervented** in apps
* The **read replica** could be set as RDS Multi-AZ for disaster recovery
![[Pasted image 20230801075444.png]]

### Benefit
---

Increase **Availability**

### Internal Steps 
---

Internal Steps happens when clicking "**Modify**" on the database:
* A snapshot is taken 
* A new DB is restored from the snapshot in a new AZ 
* Synchronization is established between the two databases
![[Pasted image 20230801075709.png]]

# Possible Cost
---

* There might be **network cost** if you need to pass the data across region. But it should be **free** when your read replica is in the same region. 