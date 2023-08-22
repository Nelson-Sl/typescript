# What's VPC Flow Logs?
---

* Capture information **about IP traffic going into your interfaces**
	* **Monitor & troubleshoot connectivity issues**

![[Pasted image 20230822200519.png]]

## Sources
---

* **VPC** Flow Logs 
* **Subnet** Flow Logs 
* **Elastic Network Interface (ENI)** Flow Logs
* Captures network information from AWS managed interfaces too
	* **ELB, RDS, ElastiCache, Redshift, WorkSpaces, NATGW, Transit Gateway**…

## Output
---

* **S3**, **CloudWatch Logs** and **Kinesis Data Firehose**

# VPC Flow Log Syntax
---

![[Pasted image 20230822201136.png]]

* **srcaddr & dstaddr** – help identify problematic IP 
* **srcport & dstport** – help identity problematic ports 
* Action – **success or failure of the request** due to Security Group / NACL

* Can be used for analytics on **usage patterns**, or **malicious behavior** 
* Query VPC flow logs **using Athena on S3** or **CloudWatch Logs Insights**

## Troubleshoot SG & NACL issues
---

![[Pasted image 20230822201537.png]]

# Architecture
---

![[Pasted image 20230822201842.png]]