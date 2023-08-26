# Networking Costs in AWS per GB - Simplified
---

* Use **Private IP** instead of Public IP for **good savings and better network performance**

![[Pasted image 20230823095003.png]]

# Minimizing egress traffic network cost
---

* Try to keep **as much internet traffic within AWS** to minimize costs
	* E.g. **Direct Connect location that are co-located in the same AWS Region** result in lower cost for egress network

![[Pasted image 20230823095328.png]]

## Concepts
---

* **Egress Traffic**: outbound traffic (from **AWS to outside**)
* **Ingress Traffic**: : inbound traffic - from **outside to AWS** (typically **free**)

# S3 Data Transfer Pricing – Analysis for USA
---

* **Ingress**: free
* **To Internet**: $0.09 per GB
* S3 Transfer Acceleration
	* **Faster transfer times** (50 to 500% better) 
	* Additional cost on top of Data Transfer Pricing: +**$0.04 to $0.08 per GB**
* S3 -> CloudFront -> Internet
	* S3 to CloudFront: **$0.00** per GB
	* CloudFront to Internet: **$0.085** per GB (slightly cheaper than S3)
		* **Caching capability** (lower latency) 
		* **Reduce costs** associated with S3 Requests Pricing (7x cheaper with CloudFront)
* S3 Cross Region Replication: **$0.02 per GB**

![[Pasted image 20230823095626.png]]

# Pricing: NAT Gateway vs VPC Endpoint
---

![[Pasted image 20230823100307.png]]
