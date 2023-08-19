# What is Cloudwatch Agent?
---

* For **virtual servers** (EC2 instances, on-premises servers…) to push the log files to cloudwatch
	* Make sure **IAM permissions are correct**

![[Pasted image 20230819201304.png]]

# Category
---

## CloudWatch Logs Agent
---

* Old version of the agent, **can only send to CloudWatch Logs**

## CloudWatch Unified Agent
---

* Collect logs & additional system-level metrics and **send to CloudWatch logs**
	* **CPU** (active, guest, idle, system, user, steal) -> out-of-box
	* **Disk metrics** (free, used, total), **Disk IO** (writes, reads, bytes, iops) -> out-of-box
	* **RAM** (free, inactive, used, total, cached)
	* **Netstat** (number of TCP and UDP connections, net packets, bytes) -> out-of-box
	* **Processes** (total, dead, bloqued, idle, running, sleep)
	* **Swap Space** (free, used, used %)
* Centralized configuration using **SSM Parameter Store**