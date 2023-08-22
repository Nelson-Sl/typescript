# What's Direct Connect?
---

* Provides a **dedicated private connection** from a remote network to your VPC
	* Dedicated connection must be setup **between your DC and AWS Direct Connect locations**
	* Supports both **IPv4** and **IPv6**

![[Pasted image 20230822211427.png]]

## Connection Types
---

* Lead times are often **longer than 1 month** to establish a new connection

### Dedicated Connections
---

* **1Gbps**,**10 Gbps** and **100 Gbps** capacity
* **Physical ethernet port** dedicated to a customer
* Request **made to AWS first**, then **completed by AWS Direct Connect Partners**

### Hosted Connections
---

* **50Mbps**, **500 Mbps**, to **10 Gbps**
* Connection requests are made via **AWS Direct Connect Partners** (**1, 2, 5, 10 Gbps available at Selected Partners**)
* Capacity can be **added** or **removed** on demand

# Direct Connect Gateway
---

* Setup a Direct Connect **to one or more VPC in many different regions** (same account)

![[Pasted image 20230822211800.png]]

# Encryption
---

* Data in transit is **not encrypted but is private**
	* AWS Direct Connect + VPN provides an **IPsec-encrypted private connection**
	* Good for **an extra level of security**, but slightly more complex to put in place

![[Pasted image 20230822212749.png]]