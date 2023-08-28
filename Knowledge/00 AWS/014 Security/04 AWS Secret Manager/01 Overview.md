# What's AWS Secret Manager?
---

* Storing secrets **with integration to RDS** (MySQL, PostgreSQL, Aurora)
	* Capability to **force rotation of secrets every X days**
		* Can automate generation of secrets on rotation (uses Lambda)
	* Secrets are **encrypted using KMS**

# Multi-Region Secret
---

* Replicate Secrets **across multiple AWS Regions**
	* Secrets Manager keeps read replicas **in sync with the primary Secret**
	* Ability to promote a read replica Secret **to a standalone Secret**
* Use cases
	* **multi-region apps**
	* **disaster recovery strategies**
	* **multi-region DB**…