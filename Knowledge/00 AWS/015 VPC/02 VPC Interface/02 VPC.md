# What's VPC?
---

* VPC stands for **Virtual Private Cloud**
	* Can have **max 5 VPCs** in an AWS region (soft limit)
	* Min CIDR size is **/28** (16 IP addresses) & Max CIDR size is **/16** (65536 IP addresses)
* Note: Your VPC CIDR **should NOT overlap with your other networks** (e.g., corporate)
# IP Range (= Private IP Range)
---

* 10.0.0.0 – 10.255.255.255 (1**0.0.0.0/8**)
* 172.16.0.0 – 172.31.255.255 (**172.16.0.0/12**)
* 192.168.0.0 – 192.168.255.255 (**192.168.0.0/16**)