# What's AWS Config?
---

* **Per-region** service that
	* Helps with **auditing and recording compliance** of your AWS resources
	* Helps **record configurations and changes** over time
	* Example
		* Is there unrestricted SSH access to my security groups?
		* Do my buckets have any public access?
		* How has my ALB configuration **changed over time**?

# How do AWS Config Works?
---

## Config Rules (For Compliance)
---

* **AWS managed config rules** (over 75)
* **Custom config rules** (must be defined in AWS Lambda)
	* Can be evaluated / triggered **for each config change** or **at regular time intervals** but does not prevent actions from happening (no deny)
	* E.g. Evaluate if **each EBS disk is of type gp2**

![[Pasted image 20230820122952.png]]

### Remidiations
---

* **Automate remediation of non-compliant resources** using **SSM Automation Documents**
	* Use **AWS-Managed Automation Documents** or create **custom Automation Documents**
	* Can set **Remediation Retries** if the resource is still non-compliant after auto-remediation

![[Pasted image 20230820124037.png]]


# Sending AWS Config Data
---
* Possibility of **storing the configuration data into S3** (analyzed by Athena)
* **Use EventBridge to trigger notifications** when AWS resources are non-compliant
* **Send configuration changes and compliance state notifications to SNS** (all events – use SNS Filtering or filter at client-side)

![[Pasted image 20230820123436.png]]

# Pricing
---

* No free tier, **$0.003 per configuration item recorded per region**,
**$0.001 per config rule evaluation per region**