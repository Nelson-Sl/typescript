# What's Site-to-Site VPN?
---

* Customer & Clients can access the resource in instance **through VPN Network**. This might **include 2 gateways to setup**.

## Virtual Private Gateway (VGW)
---

* **VPN concentrator** on the AWS side of the VPN connection & attached to the VPC from **which you want to create the Site-to-Site VPN connection**
* Possibility to **customize the ASN** (Autonomous System Number)

## Customer Gateway (CGW)
---

* **Software application** or **physical device** on **customer side of the VPN connection**

![[Pasted image 20230822203419.png]]

# How to make Site-to-Site VPN Connections?
---

* For Customer Gateway Device (On-premises), use **public internet-routable IP address** for your Customer Gateway device 
	* If it’s behind a NAT device that’s enabled for NAT traversal (NAT-T), use the **public IP address of the NAT device**
* Requirements
	* Enable **Route Propagation** for the Virtual Private Gateway in the route table that is associated with your subnets
	* If you need to **ping your EC2 instances from on-premises**, make sure you **add the ICMP protocol on the inbound of your security groups**

![[Pasted image 20230822203537.png]]

# AWS VPN CloudHub
---

* Provide **secure communication between multiple sites**, if you have multiple VPN connections
	* Goes over the **public Internet**
	* **Low-cost** hub-and-spoke model for **primary or secondary network connectivity** between different locations (VPN only)
* Set up
	* **Connect multiple VPN connections on the same VGW**, setup dynamic routing and configure route tables

![[Pasted image 20230822204220.png]]