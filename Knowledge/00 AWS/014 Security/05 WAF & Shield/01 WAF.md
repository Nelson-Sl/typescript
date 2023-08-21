# What's WAF (Web Application Firewall) ?
---

* Protects your web applications from **common web exploits (Layer 7) or HTTP**, which is deploy on:
	* **Application Load Balancer** 
	* **API Gateway** 
	* **CloudFront** 
	* **AppSync GraphQL API** 
	* **Cognito User Pool**

# Configure WAF Rules
---

* Define **Web ACL (Web Access Control List)** Rules:
	* **IP Set**: up to **10,000** IP addresses – use multiple Rules for more IPs
	* • HTTP headers, HTTP body, or URI strings Protects from common attack - SQL injection and Cross-Site Scripting (XSS)