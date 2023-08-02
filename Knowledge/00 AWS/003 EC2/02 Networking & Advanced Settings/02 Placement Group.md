# Why we use placement group?
---

With placement group we can **control over our EC2 instance placement strategy**.

# Placement group type
---

## Cluster
---

* Definition: it clusters all the instance groups **into a low-latency group in a single availability zone & racks**
* Pros & Cons
	* Pros: Great Network (**10Gbps** bandwidth between instances)
	* Cons: All instances will be failed if the rack failed
* Use cases
	* **Big Data job** that need to complete fast
	* **Application** that needs high network throughput and **extremely low latency**

## Spread
---

* Definition: spreads instances **across underlying hardware** (Max to 7 instances per AZ)
* Pros & Cons
	* Pros: Can spread into **multiple** **AZs**, **reduce risk of simultaneous failure** in application since instances are on different physical hardware
	* Cons: **Limited to 7 instances** in a single AZ per placement group
* Use Cases
	* Application that needs to **maximise high availability**
	* Critical Application where instance must **be isolated from the failure of each other**

## Partition
---

* Definition: spread instances across many different **partitions that rely on different sets of racks** (Limited to 7 partitions per AZ, and 100 instances per partition group)
	* Note: EC2 instances get access to partition information as **metadata**
* Pros & Cons
	* Pros: Can spread into **multiple AZs**, a partition failure won't effect other partitions
	* Cons: A partition failure might effect many EC2 instances within the same partition
* Use Cases: Distributed application like **HDFS / HBase / Cassandra / Kafka**