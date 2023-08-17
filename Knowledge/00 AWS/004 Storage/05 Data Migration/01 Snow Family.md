# What's Snow Family
---

* **Highly-secure, portable devices** to **collect and process data at the
edge**, and **migrate data into and out of AWS**. It includes **SnowCone**, **Snowball Edge** and **Snowmobile**

* Note: Snowball cannot import to Glacier directly, you must use Amazon S3 first, **in combination with an S3 lifecycle policy**

![[Pasted image 20230815222134.png]]

![[Pasted image 20230815222202.png]]

## SnowCone
---
* Small, portable computing device used for **edge computing**, **storage**, and **data transfer**. 
	* **8TB** HDD or **14TB** SSD Storage
	* **2 CPUs**, **4 GB** of memory, wired or wireless access
	* **USB-C power** using a cord or the optional battery
	* Support for [[05 DataSync|AWS DataSync]] to send data
* Good for **space-constrainted** environment
## SnowBall Edge
---

* Provide **block storage** and **Amazon S3-compatible object storage** with Edge computing abilities (on **EC2 Instance** & **AWS Lambda**)
	* Storage Optimized: Up to **40 vCPUs**, **80 GiB of RAM**, **80 TB storage** & Object storage clustering
	* Compute Optimized: 
		* 104 vCPUs, 416 GiB of RAM
		* **Optional GPU** (useful for video processing or machine learning)
		* **42 TB** of HDD or **28 TB** NVMe capacity

## SnowMobile
---

* Each Snowmobile has **100 PB of capacity** (use multiple in parallel) & **Transfer exabytes of data** (1 EB = 1,000 PB = 1,000,000 TBs)
	* **High security**: temperature controlled, GPS, 24/7 video surveillance
* Good for **extreme large data migration**

# How to use Snow Family
---

1. Request Snowball devices from the AWS console for delivery
2. Install the snowball client / AWS OpsHub (GUI Interface for Snowball) on your servers
3. Connect the snowball to your servers and copy files using the client
4. Ship back the device when you’re done (goes to the right AWS
facility)
5. Data will be loaded into an S3 bucket
6. Snowball is completely wiped

# Why use Snow Family
---

* Provide faster & stabler solution of **data migrating & processing** in edge location (Limited network/bandwidth/computing resource)
	* E.g. Preprocess data, Machine learning at the edge, Transcoding media streams, large data cloud migrations, DC decommission, disaster recovery