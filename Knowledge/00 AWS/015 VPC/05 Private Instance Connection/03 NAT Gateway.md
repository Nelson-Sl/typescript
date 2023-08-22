# What's NAT Gateway?
---

* **AWS-managed NAT**, higher bandwidth, high availability, no administration
	* **5 Gbps of bandwidth** with **automatic scaling up to 100 Gbps**
	* Created **in a specific Availability Zone**, uses **an Elastic IP**
	* **No Security Groups to manage / required**

# How does NAT Gateway Works?
---

* **Can’t be used by EC2 instance in the same subnet** (only from other subnets)
* Requires an **IGW** (Private Subnet => NATGW => IGW)

![[Pasted image 20230822110025.png]]

# High Availability Strategy
---

* NAT Gateway is **resilient within a single Availability Zone** & Must **create multiple NAT Gateways in multiple AZs** for fault-tolerance
* No cross-AZ failover needed because **if an AZ goes down it doesn't need NAT**

![[Pasted image 20230822110609.png]]
