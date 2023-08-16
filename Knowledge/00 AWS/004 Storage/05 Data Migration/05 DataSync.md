# What's DataSync?
---

* Move large amount of data to and from
	* **On-premises / other cloud to AWS** (NFS, SMB, HDFS, S3 API…) – needs agent
		* For Limited Bandwidth we can use [[01 Snow Family#SnowCone|SnowCone]]
	* AWS to AWS (different storage services) – no agent needed
		* S3 (And Glacier Classes), FSx, EFS

![[Pasted image 20230816192825.png]]

![[Pasted image 20230816192846.png]]

# Features
---

* Replication tasks can be scheduled hourly, daily, weekly ( **Not continuous** )
* **File permissions and metadata are preserved** (NFS POSIX, SMB…)

# Performance
---

One agent task can use **10 Gbps** ( can **setup a bandwidth limit** )