# What's Site-to-Site VPN?
---

* Customer & Clients can access the resource in instance **through VPN Network**. This might **include 2 gateways to setup**

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

* For Customer Gateway Device (On-premises) • What IP address to use? • Public Internet-routable IP address for your Customer Gateway device • If it’s behind a NAT device that’s enabled for NAT traversal (NAT-T), use the public IP address of the NAT device
![[Pasted image 20230822203537.png]]
