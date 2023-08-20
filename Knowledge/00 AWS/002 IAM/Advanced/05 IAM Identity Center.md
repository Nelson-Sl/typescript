#  What's IAM Identity Center?
---

* One login (single sign-on) for all your
	* **AWS accounts in AWS Organizations**
	* **Business cloud applications** (e.g., Salesforce, Box, Microsoft 365, …)
	* **SAML2.0-enabled applications**
	* **EC2 Windows Instances**

![[Pasted image 20230820151651.png]]

![[Pasted image 20230820151805.png]]

## Identity Provider
---

* **Built-in identity store** in IAM Identity Center
* 3rd party: **Active Directory (AD)**, **OneLogin**, **Okta**…

# Security: Fine-grained Permissions and Assignments
---

## Multi-Account Permissions
---

* **Manage access across AWS accounts** in your AWS Organization
* Permission Sets – a collection of **one or more IAM Policies assigned to users and groups** to define AWS access
![[Pasted image 20230820151919.png]]

## Application Assignments
---

* **SSO access to many SAML 2.0 business applications** (Salesforce, Box, Microsoft 365, …)