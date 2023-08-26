# What's Bastion Host?
---

* Bastion Host is an instance in the public subnet which is then **connected to all other private subnets** & allow to **SSH into our private EC2 instances**

![[Pasted image 20230821223134.png]]

# Prerequisite to Make Bastion Host Works
---

* Bastion Host security group **must allow inbound from the internet on port 22 from restricted CIDR** for security reason
	* E.g. the public CIDR of your corporation
* Security Group of the EC2 Instances **must allow the Security Group of the Bastion Host**, or **the private IP of the Bastion host**