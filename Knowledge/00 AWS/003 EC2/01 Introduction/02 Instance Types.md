# Naming Conventions
---

![[ec2_instance.png]]
E.g. **m5.2xlarge**
* **m**: [[02 Instance Types|Instance Class]]
* **5**: version of EC2 Instances (AWS Keeps improving instance)
* **2xlarge**: size within the instances (E.g. micro, large, 2xlarge)

# Instance Types/Class
---

* References
	* [Amazon EC2 Instance Comparison (vantage.sh)](https://instances.vantage.sh/)
	* https://aws.amazon.com/ec2/instance-types

## General Purpose
---

* **Balance** between memory, networking and compute
* Can be used for **a variety of diverse workloads**, fits for **web servers** and **code repositories**
* E.g. t2.micro, Mac, M7g

## Compute Optimized
---

* More emphasis for compute
* Can be used for **compute-intensive tasks** that require high performance processors
* Use Cases
	* **Batch processing workloads**
	* Media Transcoding
	* High-performance web servers
	* **High-performance computing (HPC)**
	* **Machine Learning & Scientific Modeling**
	* Dedicated gaming servers
* E.g. C7g

## Memory Optimized
---

* More emphasis on memory
* Fast performance for workloads that processing large datasets in memory (Data Processing)
* Use Cases
	* High performance **relational/non-relational databases**
	* Distributed web **scale cached stores**
	* In-memory databases optimized for **BI** (Business Intelligence)
	* Application performing **real-time processing of big unstructured data**
* E.g. X1, R6g

## Storage Optimized
---

* More emphasis on storage
* Can be used for **storage-intensive tasks** that require **high, sequential read and write access to large data sets** on local storage
* Use cases
	* Relational & No-SQL **Databases**
	* **Cache** for in-memory databases (E.g. Redis)
	* High frequency **online transaction processing (OLTP)** system
	* **Data Warehouse** applications
	* Distributed **file systems**
* E.g. L4g, Lm4gn, D2