# What's ACM?
---

* Easily **provision, manage, and deploy TLS Certificates**, provide **in-flight encryption for websites (HTTPS)**
	* **Automatic TLS certificate renewal**

![[Pasted image 20230821172451.png]]

# Requesting & Importing Certificates
---

## Requesting
---

1. List domain names to be included in the certificate 
	* **Fully Qualified Domain Name (FQDN)**: corp.example.com 
	* **Wildcard Domain**: *.example.com
2. Select Validation Method: **DNS Validation** or **Email validation**
	* DNS Validation will **leverage a CNAME record** to DNS config (ex: Route 53), preferred for **automation purposes**
	* Email validation will **send emails to contact addresses** in the WHOIS database
3. It will take **a few hours to get verified**
4. The Public Certificate will be enrolled for automatic renewal
	* ACM automatically **renews ACM-generated certificates 60 days** before expiry

* Note
	1. Option to **generate the certificate outside of ACM** and then import it, but should be **no renewal** and **must import a new certificate before expiry**
	2. ACM sends daily expiration events **starting 45 days prior to expiration**
		* The # of days can be configured by `acm-certificate-expiration-check`
		* Events are appearing in **EventBridge**

## Importing
---


![[Pasted image 20230821182946.png]]

# Integration
---

## Integration with ALB
---

 ![[Pasted image 20230821183526.png]]


## Integration with API-Gateway
---

* Create a **Custom Domain Name** in API Gateway
	* **Edge-Optimized** (default): For global clients
		* The TLS Certificate **must be in the same region as CloudFront**, in **us-east-1**
	* **Regional**
		* The TLS Certificate must be imported on API Gateway, **in the same region as the API Stage**
* Then setup **CNAME or (better) A-Alias record** in Route 53
