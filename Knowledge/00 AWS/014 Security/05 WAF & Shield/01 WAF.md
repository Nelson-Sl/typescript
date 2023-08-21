# What's WAF (Web Application Firewall) ?
---

* Protects your web applications from **common web exploits (Layer 7) or HTTP**, which is deploy on:
	* **Application Load Balancer** 
	* **API Gateway** 
	* **CloudFront** 
	* **AppSync GraphQL API** 
	* **Cognito User Pool**
* A regional service except **CloudFront**

# Configure WAF Rules
---

* Define **Web ACL (Web Access Control List)** Rules:
	* **IP Set**: up to **10,000** IP addresses – use multiple Rules for more IPs
	* HTTP headers, HTTP body, or URI strings Protects from common attack - **SQL injection** and **Cross-Site Scripting (XSS)**
	* Size constraints, **geo-match** (block countries)
	* **Rate-based rules (to count occurrences of events)** – for DDoS protection

## Rule Group
---

* A **reusable set of rules that you can add to a web ACL**

# Use Case: Fixed IP while using WAF with a Load Balancer
---

* Since WAF **does not support the Network Load Balancer** (Layer 4), we can use **Global Accelerator for fixed IP** and WAF on the ALB

![[Pasted image 20230821193233.png]]
