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

# Sending AWS Config Data
---
* Possibility of **storing the configuration data into S3** (analyzed by Athena)
* **Use EventBridge to trigger notifications** when AWS resources are non-compliant
* **Send configuration changes and compliance state notifications to SNS** (all events – use SNS Filtering or filter at client-side)