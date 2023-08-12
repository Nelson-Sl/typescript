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
* Routing Policy -> **How Route 53 respond to queries**
* [[05 TTL (Time to Live)|TTL (Time to Live)]]