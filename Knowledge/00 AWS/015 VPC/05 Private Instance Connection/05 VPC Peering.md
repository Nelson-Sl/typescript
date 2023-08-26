# What's VPC Peering?
---

* **Privately connect two VPCs** using AWS’ network & Make them behave **as if they were in the same network**
	* Must **not have overlapping CIDRs**
	* Must **update route tables in each VPC’s subnets** to ensure EC2 instances can communicate with each other

![[Pasted image 20230822191124.png]]

# Note / Good to Know
---

* VPC Peering connection **is NOT transitive** (must be established for each VPC that need to communicate with one another
* Can create VPC Peering connection between VPCs **in different AWS accounts/regions**
* Can **reference a security group in a peered VPC** (works cross accounts – same region)

![[Pasted image 20230822191008.png]]

![[Pasted image 20230822191032.png]]