# Definition
---

Acting like a firewall, security groups controls how traffic is **allowed into** or **out of** our EC2 Instances. It regulates:
* Control of **inbound network** (from outside to instance) and **outbound network** (from instance to outside)
* Access to **Ports**
* Authorized **IP ranges / addresses** - IPv4 and IPv6

![[security_group.png]]

# Characteristics & Good to Know
---

* Security groups only contains **allow** rules
* Security group rules could be referenced by **IP** and **security group**
* Security group can **be attached to multiple instances**
* Security group is **locked down to a region / VPC combination**
* Security group **"lives" outside EC2** -> If traffic is blocked by security group then EC2 won't see it
* By Default, security group **blocks all inbound traffic** and **authorized all outbound traffic**

# Best Practice & Troubleshoot
---

* It's good to **maintain one seperate group for SSH access** (SSH Connection is complicated)
* If an application is **not accessible** or **timeout**, then it's a security group issue
* If an application shows error of **refusing to connect**, then it's an application issue

# Classic Ports
---

* Port **80** (HTTP): Access unsecured website
* Port **443** (HTTPS): Access secured website
* Port **21** (FTP - File Transfer Protocol): Upload files to a shared folder
* Port **22** 
	* SSH - Secure Shell: Log in to a Linux instance
	* SFTP - Secure File Transfer Protocol: Upload files using SSH
* Port **3389** (RDP - Remote Desktop Protocol): Log into a Windows instance
