# Definition
---

An Elastic Load Balancer in Layer 3 (Network Layer) to deploy, scale and manage a fleet of 3rd party **network virtual appliances** in AWS, Which Supports following target groups:
* **EC2 instances**
* **IP Addresses** – must be private IPs (If virtual appliances is on your own machine)

It used the **GENEVE** protocols on Port **6081**

![[Pasted image 20230718230903.png]]

# Components
---

* **Transparent Network Gateway** – single entry/exit for all traffic
* **Load Balancer** – distributes traffic to your virtual appliances

# Use Cases
---

* **Firewalls**
* **Intrusion Detection & Prevention** Systems
* **Deep Packet Inspection** Systems
* **Payload Manipulation**