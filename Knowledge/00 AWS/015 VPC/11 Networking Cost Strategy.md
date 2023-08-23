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
* To Internet: $0.09 per GB

![[Pasted image 20230823095626.png]]

