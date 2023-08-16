# Definition
---

* An AWS managed service to **launch 3rd party high-performance file systems** on AWS

# Category
---

## FSx for Windows File Server
---

* Can be mounted on **Linux EC2 instances**
* **Support System Protocol**
	* SMB
	* Windows NTFS
	* Microsoft's Distributed File System (DFS) Namespaces
* **Storage** 
	* Scale up to **10s of GB/s, millions of IOPS, 100s PB of data**
	* Options
		* SSD - **latency sensitive workloads**
		* **HDD** - **broad spectrum of workloads**
* **Advantage**
	* Can be **accessed from your on-premises infrastructure** (VPN or Direct Connect)
	* Can be configured to be **Multi-AZ** (high availability)
	* Data is **backed-up daily** to S3

## FSx for Lustre
---

* A type of **parallel distributed file system**, for large-scale computing
* **Storage**
	* Scales up to **100s GB/s, millions of IOPS, sub-ms latencies**
	* Options
		* **SSD** - **low-latency, IOPS intensive workloads**, small & random file operations
		* **HDD** - **throughput-intensive workloads**, large & sequential file operations
* FS Options
	* Stratch File System
		* **High burst** (6x faster, 200MBps per TiB)
		* **Temporary storage** & Data is not replicated (doesn’t **persist if file server fails**)
		* Use Case: **short-term processing**, **optimize costs**
	* Persistent File System
		* Long-term storage & Data is replicated within same AZ (within few Minutes)
		* Use Case: **long-term processing**, **sensitive data**
* Advantage
	* Can be **accessed from your on-premises infrastructure** (VPN or Direct Connect)
	* Seamless integration with S3
		* Can “**read S3**” as a file system (through FSx)
		* Can **write the output of the computations back to S3** (through FSx)
* Use Case
	* Machine Learning, **High Performance Computing (HPC)**
	* **Video Processing**, **Financial Modeling**, **Electronic Design Automation**

## FSx for NetApp ONTAP
---

* Move workloads **running on ONTAP or NAS** to AWS
* Support System Protocol
	* **NFS**, **SMB**, **iSCSI**
* Advantage
	* Auto-Scaling: Storage **shrinks or grows automatically**
	* Snapshots, replication, low-cost, compression and data de-duplication
	* Point-in-time **instantaneous cloning** (helpful for testing new workloads)
* Support Platform
![[Pasted image 20230816175847.png]]

## FSx for OpenZFS
---

* Move **workloads running on ZFS** to AWS
* Support System Protocol: **NFS**