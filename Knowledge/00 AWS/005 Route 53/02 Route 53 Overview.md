# What is Route 53?
---

Route 53 is a service **fully managed by AWS**:
* Highly **Available**, **Scalable** & **Authoritative** DNS system ( Users can **update DNS Records** )
* **Domain Registerar**
* Provide **100% Availability SLA**

![[Pasted image 20230809232405.png]]

# Route 53 Records
---

Defines how you want to **route the traffic for a domain**. This includes:
* **Domain Name / Sub Domain Name** -> E.g. example.com
* [[03 Record Type|Record Type]]
* Value -> E.g. 12.34.56.78
* [[07 Routing Policy|Routing Policy]] -> **How Route 53 respond to queries**
* [[05 TTL (Time to Live)|TTL (Time to Live)]]

# Working with 3rd Party Domain Registrar
---

* Even though domain registrar usually **provide DNS service to manage your DNS record**, but you can **choose Route 53 as your DNS service as well**. ( E.g. **purchase the domain from GoDaddy** and **use Route 53 to manage your DNS records** )
	* Steps
		* 1. Create a [[04 Hosted Zones|Hosted Zone]] in Route 53
		* 2. **Update NS Records on 3rd party website** to use Route 53 Name Servers

![[Pasted image 20230814000150.png]]
