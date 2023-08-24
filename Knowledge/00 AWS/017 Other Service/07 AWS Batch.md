# What is AWS Batch?
---

* **Fully managed batch processing** at any scal\
	* Efficiently run **100,000s of computing batch jobs** on AWS
	* Defined as **Docker images** and **run on ECS**

# How does AWS Batch Works?
---

* Batch will **provisions the right amount of compute / memory**, and **dynamically launch EC2 instances** or **Spot Instances**
* **Submit or schedule batch jobs** and AWS Batch does the rest

![[Pasted image 20230824195323.png]]

# Batch vs Lambda
---

* Time Limit
	* Batch has no time limit, lambda has **longest duration of 15 mins**
* Runtime
	* Lambda has **limited runtime**, batch will have **any runtime as long as it’s packaged as a Docker image**
* Disk Space
	* Lambda has **limited temporary disk space**, while Batch **rely on EBS / instance store for disk space**
* Serverless
	* Lambda is **serverless**, while **batch relies on EC2** (can be managed by AWS)