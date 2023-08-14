# User-Based: IAM Policies
---

Restrict access based on **which API calls should be allowed for a specific user from IAM**

![[Pasted image 20230814210811.png]]

![[Pasted image 20230814211325.png]]

# Resource-Based
---

## Bucket Policy
---

* **JSON-Based**, **bucket wide rules** from the S3 console
* Use Cases
	* Grant **public access** to the bucket
	* Grant **access to another account** (Cross Account)
	* Force objects **to be encrypted at upload**

![[Pasted image 20230814211656.png]]

![[Pasted image 20230814211627.png]]

## Object / Bucket Access Control List (ACL)
---

* Use to prevent company data leaCan be **set at account level** & **disabled**
* 