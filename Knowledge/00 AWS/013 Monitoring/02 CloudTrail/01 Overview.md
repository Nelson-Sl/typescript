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

* Detect **unusual activity in your account**:
	* inaccurate resource provisioning
	* hitting service limits
	* Bursts of AWS IAM actions
	* Gaps in periodic maintenance activity

![[Pasted image 20230820110456.png]]

### How to log Insights?
---

* CloudTrail Insights analyzes normal management events to **create a baseline**, then **continuously analyzes write events to detect unusual patterns**
	* Anomalies appear in the CloudTrail console
	* Event is sent to Amazon S3
	* An EventBridge event is generated (for automation needs)

## Retention Period
---

* Events are **stored for 90 days** in CloudTrail
* To keep events beyond this period, **log them to S3 and use Athena**

![[Pasted image 20230820110728.png]]
