# What's CloudTrail?
---

* Provides **governance, compliance and audit** for your AWS Account
* Enabled by Default

# How does CloudTrail Works?
---

* A trail can be **applied to All Regions (default)** or a **single Region**

![[Pasted image 20230820105229.png]]

# CloudTrail Events
---

## Management Events (By Default)
---

 * Operations that **are performed on resources in your AWS account**
	 * Configuring security (IAM AttachRolePolicy)
	 * Configuring rules for routing data (Amazon EC2 CreateSubnet)
	 * Setting up logging (AWS CloudTrail CreateTrail)
 * Can **separate Read Events** (that don’t modify resources) from **Write Events** (that may modify resources)

## Data Events
---

* Amazon **S3 object-level activity** (ex: GetObject, DeleteObject, PutObject, Execution)
* can separate Read and Write Events

## Insight Log Events
---

