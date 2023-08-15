# What's Global Accelerator?
---

* Global Accelerator is a service that **leverage the AWS internal network** to route to your application

# How Global Accelerator Works
---

1. **2 Anycast IP** are created for your application (i.e. AnyCast IP: all servers **hold the same IP address** and **the client is routed to the nearest one**)
2. The Anycast IP send traffic directly to **Edge Locations**
3. The Edge locations send the traffic to your application

Note: Works with **Elastic IP**, **EC2 instances**, **ALB**, **NLB**, public or private

![[Pasted image 20230815211607.png]]

# Feature
---

* Security
	* **DDoS protection** thanks to AWS Shield
* Health Check
	* Help for **disaster recovery & Fast Failover**

# Why use Global Accelerator?
---

* Provide Consistent Performance based on
	* Intelligent routing to **lowest latency** and **fast regional failover**
	* **No issue with client cache** (because the IP doesn’t change)
	* Internal AWS network