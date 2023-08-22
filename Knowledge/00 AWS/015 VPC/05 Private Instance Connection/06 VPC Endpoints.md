# What's VPC Endpoint?
---

* VPC Endpoints (powered by **AWS PrivateLink**) allows you to **connect to AWS services using a private network** instead of using the public Internet
	* Every AWS service is **publicly exposed** (public URL)
	* **Redundant** and **scale horizontally**

![[Pasted image 20230822193049.png]]

![[Pasted image 20230822193259.png]]

# Types of Endpoints
---

## Interface Endpoints (powered by PrivateLink)
---

* **Provisions an ENI (private IP address) as an entry point** (must attach a Security Group)
* Supports **most AWS services**
* Charge: $ per hour + $ per GB of data processed
* Preferred when **access is required from on-premises** (Site to Site VPN or Direct Connect), **a different VPC or a different region**

![[Pasted image 20230822193756.png]]

## Gateway Endpoints
---

* **Provisions a gateway** and **must be used as a target in a route table** (does not use security groups)
* Supports **S3 & DynamoDB**
* Free, Mostly Preferred

![[Pasted image 20230822194031.png]]

# Checking Issues
---

* Check **DNS Setting Resolution** in your VPC 
* Check **Route Tables**