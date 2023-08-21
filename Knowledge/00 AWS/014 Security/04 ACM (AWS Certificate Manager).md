# What's ACM?
---

* Easily **provision, manage, and deploy TLS Certificates**, provide **in-flight encryption for websites (HTTPS)**
	* **Automatic TLS certificate renewal**

![[Pasted image 20230821172451.png]]

# Requesting Certificates
---

## Public Certificates
---

1. List domain names to be included in the certificate 
	* **Fully Qualified Domain Name (FQDN)**: corp.example.com 
	* **Wildcard Domain**: *.example.com
2. Select Validation Method: **DNS Validation** or **Email validation**
	* DNS Validation will **leverage a CNAME record** to DNS config (ex: Route 53), preferred for **automation purposes**
	* Email validation will **send emails to contact addresses** in the WHOIS database
3. It will take **a few hours to get verified**
4. The Public Certificate will be enrolled for automatic renewal
	* ACM automatically renews ACM-generated certificates 60 days before expiry