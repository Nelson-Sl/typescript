# What's Transit Gateway?
---

* For **having transitive peering between thousands of VPC and on-premises**, hub-and-spoke (star) connection
	* Regional resource, but can **share cross-account** using Resource Access Manager (RAM) & **peer Transit Gateways across regions**
	* Supports **IP Multicast** (not supported by any other AWS service)

![[Pasted image 20230822214339.png]]

# Use Cases
---

## Site-to-Site VPN ECMP (Equal-cost multi-path routing)
---

* Routing strategy to **allow to forward a packet over multiple best path**
* Can create **multiple Site-to-Site VPN connections** to increase the bandwidth of your connection to AWS

![[Pasted image 20230822214823.png]]

![[Pasted image 20230822214959.png]]

## Share Direct Connect between multiple accounts
---

![[Pasted image 20230822215046.png]]
