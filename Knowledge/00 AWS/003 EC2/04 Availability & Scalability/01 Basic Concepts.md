# Availability, Scalability & Scaling
---

![[Pasted image 20230711192928.png]]

# Load Balancer
---

## Definition
---

Servers that forward traffic to multiple servers (E.g. EC2 Instances) downstream

## Reason to Use Load Balancer
---
* Availability & Scalability 
	* Spread load across multiple downstream instances 
	* Seamlessly handle failures of downstream instances
	* High availability across AZs 
* Security & Traffic Control
	* Expose a single point of access (DNS) to your application 
	* Do regular health checks to your instances (Using port and route E.g. Port 4567, route /health)
	* Provide SSL termination (HTTPS) for your websites 
	* Separate public traffic from private traffic
* Other
	* Enforce stickiness with cookies 
