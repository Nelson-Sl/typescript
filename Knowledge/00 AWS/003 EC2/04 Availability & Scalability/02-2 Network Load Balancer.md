# Definition
---

An Elastic Load Balancer in Layer 4 (TCP/UDP), Which Supports:
* Traffic from **TCP/UDP**
* Load balancing to multiple TCP/UDP Connections, where the target groups could be one of following:
	* **EC2 instances**
	* **Lambda functions**
	* **IP Addresses** – must be **private IPs**
	* **Application Load Balancer** - Helpful for **whitelisting specific IPs**

Hostname: **XXX.{{region}}.elb.amazonaws.com**

# Features
---

## Routing
---

![[Pasted image 20230718225116.png]]

## Fixed/Static IP
---

Network Load Balancer has **one static IP** per Availability zone, and also can assign Elastic IP.

## Health Check
---

Can Support Health Check from **TCP, HTTP, HTTPS** connection

# Benefit
---

Since it could handle millions of requests within second with **low latency** (Approx. 100ms), it could be helpful to use for TCP/UDP connections with **extreme performance**