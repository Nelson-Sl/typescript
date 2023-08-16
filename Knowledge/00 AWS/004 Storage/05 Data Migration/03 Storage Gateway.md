# What's Storage Gateway?
---

* Bridge between **on-premises data** and **cloud data**

![[Pasted image 20230816183326.png]]

# Prerequisite: Hardware & Software
---

* on-premises **virtualization** (E.g. EC2, Microsoft Hyper-V, Linux KVM, VMWare ESXi) 
* Hardware Appliance
	* can buy it on amazon.com
	* Has the required **CPU, memory, network, SSD cache resources**
	* Helpful for **daily NFS backups** in small data centers

# How Storage Gateway Works?
---

* S3 File Gateway
	* **Most recently used data is cached** in the file gateway
	* SMB Protocol **has integration with Active Directory (AD)** for user authentication
* FSx File Gateway
	* **Local cache** for frequently accessed data
	* **Windows native compatibility** (SMB, NTFS, Active Directory...)
	* Use Case: **Group File Shares** & **Home Directories**
* Volume Gateway
	* Use Case: **Backed by EBS snapshots** which can help restore on-premises volumes

![[Pasted image 20230816183717.png]]
