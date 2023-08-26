# What's Network Firewall?
---

* Protect your **entire Amazon VPC** & From **Layer 3 to Layer 7 protection**, can inspect several traffics:
	* **VPC to VPC traffic** 
	* **Outbound to internet** 
	* **Inbound from internet** 
	* **To / from Direct Connect & Site-to-Site VPN**
* Uses the **AWS Gateway Load Balancer**

![[Pasted image 20230823101208.png]]

# Rules & Fine-Grained Controls
---

* Supports **1000s of rules** & can be **centrally managed cross-account by AWS Firewall Manager** to apply to many VPCs
	* E.g.
		* **IP & port** - example: 10,000s of IPs filtering
		* **Protocol** – example: block the SMB protocol for outbound communications
		* **Stateful domain list rule groups**: only allow outbound traffic to *.mycorp.com or third-party software repo
		* **General pattern matching** using regex
* Traffic filtering: **Allow, drop, or alert for the traffic** that matches the rules
* **Active flow inspection** to **protect against network threats with intrusion-prevention** capabilities (like Gateway Load Balancer, but all managed by AWS)

# Logs & Analysis
---

* Send logs of rule matches to **Amazon S3, CloudWatch Logs, Kinesis Data Firehose**