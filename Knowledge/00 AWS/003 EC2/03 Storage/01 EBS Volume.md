# What is EBS?
---

An EBS Volume is a **network drive** that allows you to attach to your instances while they run (or detach). It allows your instance to **persist data** even after the termination

# Characteristics & Good to Know
---

* A EBS Volume can only **be attached to one instance** at a point of time (Except io1/io2 with [[01 EBS Volume#EBS Multi-Attach|EBS Multi-attach]] feature)
* EBS Volume is bounded in **specific availability zone** (AZ)
* Have a **provisioned capacity** (in IOPS/GB) and can be increased over time
* By default, when the instance has been terminated, **root EBS** will be deleted and the **attached EBS** won't be deleted. But it could be controlled at management console
	* Use case: **preserve root volume** when instance is terminated

# EBS Volume Types
---

* **General Purpose SSD** (gp2/gp3): **balance price and performance** for a variety of workloads
* **Provisioned IOPS SSD** (PIOPS, io1/io2/io2 Block Express): mission-critical **low-latency** or **high-throughput** workloads (E.g. database workloads)
	* Has [[01 EBS Volume#EBS Multi-Attach|EBS Multi-attach]] feature
	* io2 to io1: Higher **durability** & more **IOPS/GB**
* **Throughput-Optimized HDD** (st1): **frequently accessed**, **throughput-optimized** workloads (E.g. logging, big data)
* **Cold HDD** (sc1): **less frequently-accessed** & **cost-efficient** workloads
![[ebs_volume_types_1.png]]
![[ebs_volume_types_2.png]]

# Features
---

## EBS Multi-Attach
---

It allows a EBS Volume to **be attached to multiple instances** (up to 16 instances) in the same AZ. (Only supports in **io1/io2** family)
* Note
	* Each instance has full **read/write** permission
	* Must use a file system that is **cluster-aware** (not XFS, EXT4...)

### Use Cases
---

* **Higher application availability** in clustered Linux Applications (E.g. Teradata)
* Applications/Workloads that needs to **manage concurrent write operations**

## Encryption
---

When EBS needs encryption, it will leverage a key from KMS (With **AES-256** Algorithm). And that means the following stuffs should be encrypted:
* Data **inside the EBS Volume**
* Data that have a **flight move between EC2 Instance and EBS Volume**
* All **snapshots** created by volume
* All volume **created by encrypted snapshot**

Note: 
* Encryption has **little effect** on the latency
* Copying of an unencrypted snapshot **allows encryption**

# Backup Tool: EBS Snapshot
---

## What is EBS Snapshot?
---

EBS Snapshot allows you to **make a backup on your EBS volume** at a point of time, so that **you can move it across AZ or region**.

## Features
---

### EBS Snapshot Archive
---

It will move snapshot to "archive tier" which is **75% cheaper**. Usually it will take 24-72 hours to restore the archived snapshot

### EBS Snapshot Recycle Bin
---

Can set up retention rules to **retain/recover deleted snapshots** so that you can recover them from an accidental deletion (1 day - 1 year)

### Fast Snapshot Restore (FSR)
---

Force **full initialization of snapshot** to have no latency on the first use (cost a lot of money)