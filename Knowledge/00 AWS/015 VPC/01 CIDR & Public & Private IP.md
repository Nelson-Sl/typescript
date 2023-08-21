# What's CIDR?
---

* CIDR stands for **Classless Inter-Domain Routing**, is a method to **allocate IP addresses**
	* help to **define an IP address range**
	* Used in **Security Groups rules** and **AWS networking in general**

![[Pasted image 20230821211546.png]]

# How CIDR-IPv4 works?
---

* CIDR consists of two components
	* Base IP: Represents an **IP contained in the range**
		* E.g. **10.0.0.0**, **192.168.0.0**, …
	* Subnet Mask: Defines **how many bits can change in the IP**
		* E.g. /0, /24. /32

![[Pasted image 20230821211855.png]]

# Public vs Private IPv4
---

* Established by **The Internet Assigned Numbers Authority (IANA)**
* Private IP can only allow certain values: 
	* 1**0.0.0.0 – 10.255.255.255** (10.0.0.0/8) - in big networks 
	* **172.16.0.0 – 172.31.255.255** (172.16.0.0/12) - AWS default VPC in that range 
	* **192.168.0.0 – 192.168.255.255** (192.168.0.0/16) - e.g., home networks