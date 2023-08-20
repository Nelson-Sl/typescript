# What is SSM Parameter Store?
---

* Secure storage for **configuration and secrets**
	* Serverless, scalable, durable, easy SDK
	* **Version tracking** of configurations / secrets

## Integration
---

* Security through **IAM**
* Optional Seamless Encryption using **KMS**
* Notifications with **Amazon EventBridge**
* Integration with **CloudFormation**

# Store Hierarchy
---

![[Pasted image 20230820191621.png]]

# Tiers: Standard & Advanced
---

* Advanced: **More parameters allowed**, **larger size of parameter value**, **Allow to add parameter policy**

![[Pasted image 20230820191720.png]]

## Parameters Policies (for advanced parameters)
---

* Allow to **assign a TTL to a parameter** (expiration date) to **force updating or deleting sensitive data** such as passwords
* Can assign **multiple policies at a time**

![[Pasted image 20230820192147.png]]
