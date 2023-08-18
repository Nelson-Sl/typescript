# How do lambdas work with VPC?
---

* By default, your Lambda function is launched **outside your own VPC** (in an AWS -owned VPC), therefore **cannot access resources in your VPC** (RDS, ElastiCache, internal ELB…)
* To access VPC in lambda, you must **define the VPC ID, the Subnets and the Security Groups**, then Lambda **will create an ENI (Elastic Network Interface) in your subnets**

![[Pasted image 20230818110951.png]]

![[Pasted image 20230818111013.png]]

# Use Case: Lambda with RDS Proxy
---

* [[06 RDS Proxy#How RDS Proxy Works?|Lambda with RDS Proxy]]
* Advantage:
	* Improve scalability by **pooling and sharing DB connections**
	* Improve availability by **reducing by 66% the failover time and preserving connections**
	* Improve security by **enforcing IAM authentication and storing credentials in Secrets Manager**