# What's Firewall Manager
---

* Manage rules **in all accounts of an AWS Organization**

# Setting Rules: Security Policy
---

* Setting **common set of security rules** (applied to new resources as they are created (good for compliance) **across all and future accounts in your Organization**):
	* **WAF rules** (Application Load Balancer, API Gateways, CloudFront)
	* **AWS Shield Advanced** (ALB, CLB, NLB, Elastic IP, CloudFront)
	* **Security Groups for EC2**, **Application Load Balancer** and **ENI resources in VPC**
	* **AWS Network Firewall** (VPC Level)
	* Amazon **Route 53 Resolver DNS Firewall**
* Policies are **created at the region level**