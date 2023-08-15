# Solving Session Issue
---

## ELB Sticky Session
---

* Pros
	* Keep the session for the same AZ
* Cons
	* Lost session when AZ fails

![[Pasted image 20230814123715.png]]

## User Cookies
---

* Pros
	* No need to store session at instance side
* Cons
	* HTTP Request should be **heavier**
	* Cookies can be altered (**Security Risk**)
	* Cookies **should be validated** & **less than 4KB**

![[Pasted image 20230814124212.png]]

## Server Session
---

![[Pasted image 20230814124640.png]]

# Store Data in Database
---

## Choose Storage
---

### Single Instance Application: EBS
---

![[Pasted image 20230814193954.png]]

### Distributed Application: EFS
---

* Share same data **cross availability zone**

![[Pasted image 20230814194048.png]]
## Scaling Reads
---

### Read Replica
---

![[Pasted image 20230814125054.png]]

### Lazy Loading
---

* **Less Read Request to RDS** but may **get outdated data**

![[Pasted image 20230814125240.png]]

### Aurora
---

* Easy Scaling by **Multi AZ** & **Read Replica**

![[Pasted image 20230814193744.png]]

## FailOver: Multi AZ for RDS & ElasticCache
---

![[Pasted image 20230814125403.png]]

# Improve Security: Security Group
---

![[Pasted image 20230814125504.png]]
