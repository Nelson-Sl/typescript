# How EC2 Hibernate Works?
---

Given the fact that the in-memory (RAM) state is preserved, with the adoption of EC2 hibernate, the RAM state will be **written to a file in the ROOT EBS volume**, therefore **the instance boot will be much faster**.

Note: An instance can't be hibernated **for more than 60 days**

# EC2 Hibernate Use Cases
---

* **Long-Run processing**
* Services that **take time to initialize**
* Just want to **save RAM state**

# Requirements on EC2 Hibernate
---

* Instance Families: **C3, C4, C5, I3, M3, M4, R3, R4, T2, T3, etc.**
* Instance Types: [[04 Purchasing Options#EC2 On Demand|On-Demand]], [[04 Purchasing Options#EC2 Reserved Instances|Reserved]] and [[04 Purchasing Options#EC2 Spot Instance|Spot Instance]]
* AMI/OS: **Amazon Linux 2, Linux AMI, Ubuntu, RHEL, Centos & Windows, etc.**
	* Note: Not support for bare metal instances
* RAM Size: **< 150 GB**
* Root Storage / Volume: **EBS, Encrypted & Large**