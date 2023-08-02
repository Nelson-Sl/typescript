# What is EFS?
---

EFS (Elastic File System) is a managed NFS (Network File System) that **can be mounted for many EC2 Instances** in different AZs.

# Characteristics & Features
---

* Highly **available**, **scalable**, **expensive** (3*gp2), pay per use
* Use NFS v4.1 protocol
* Use **security group** to control access to NFS
* Use **KMS key** for encryption
* Only compatible with **Linux-Based AMI** since it uses POSIX File System
* **Auto Scaling** to petabyte-scale NFS with **10GB+/s** throughput, No capacity planning

# Use Cases
---

Content Management, Web Serving, Data Sharing, Wordpress, etc.

# Configuration
---
* Performance Mode: **General Purpose** (Latency-sensitive cases, E.g. Web Server, CMS) vs **Max I/O** (Higher latency & throughput, E.g. Big data, Media Processing)
* Throughput Mode
	* **Bursting**: E.g. 1TB Storage, 50MB/s and burst to up to 100MB/s
	* **Provisioned**: Fix throughput regardless of storage
	* **Elastic:** Automatically scale throughput up & down based on your workloads (Up to **3GB/s for read & 1GB/s for write**, can be used for unpredictable workloads)
* Storage Tiers (Move File After N days)
	* Standard: store **frequently-accessed** files
	* EFS-IA (Infrequently access): store **infrequently-accessed** files with **a lower price to store** and **cost to retrieve**. Can accessed through a **lifecycle policy** 
* Availability & Durability
	* Standard: Run for Multiple AZs, good for **prod**.
	* One Zone: Run for specific AZs with **EFS-IA** and **backup** features opened, good for dev and can get up to 90% savings