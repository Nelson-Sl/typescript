# What's AWS Inspector?
---

* A Fully Managed service for **automated security assessment**

# Integrated Service
---

## EC2 instances
---

* Leveraging the **AWS System Manager (SSM) agent**
* Analyze against **unintended network accessibility** & running OS against **known vulnerabilities**

## Container Images push to Amazon ECR
---

* **Assessment of Container Images** as they are pushed

## Lambda Functions
---

* Identifies **software vulnerabilities** in function code and package dependencies
* **Assessment of functions** as they are deployed

![[Pasted image 20230821202029.png]]

# What does Amazon Inspector evaluate?
---

* Continuous **scanning of the infrastructure**, only when needed
	* **Package vulnerabilities** (EC2, ECR & Lambda) – database of CVE
	* **Network reachability** (EC2)
* A **risk score** is associated with all vulnerabilities for prioritization