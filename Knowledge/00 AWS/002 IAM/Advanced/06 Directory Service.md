# Prerequisite: Microsoft AD Services
---

* Found on **any Windows Server with AD Domain Services**
	* Database of objects: User Accounts, Computers, Printers, File Shares, Security Groups
	* Organized by **Tree**
	* **Centralized security management**: create account, assign permissions

![[Pasted image 20230820154748.png]]

# Directory Service in AWS
---

## AWS Managed Microsoft AD
---

* **Create your own AD in AWS**, manage users
locally, supports MFA
* **Establish “trust” connections** with your on-
premises AD

![[Pasted image 20230820155026.png]]

## AD Connector
---

* Directory Gateway (proxy) to **redirect to on-premises AD**, supports MFA
* Users are **managed on the on-premises AD**

![[Pasted image 20230820155242.png]]

## Simple AD
---

* **AD-compatible managed directory** on AWS
* **Cannot be joined with on-premises AD**

![[Pasted image 20230820155446.png]]
