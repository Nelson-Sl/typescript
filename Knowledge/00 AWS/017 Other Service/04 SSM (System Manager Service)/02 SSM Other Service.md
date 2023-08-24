# Run Command
---

* **Execute a document** (= script) or **just run a command** across multiple instances (using resource groups)
	* No need for SSH

![[Pasted image 20230824191314.png]]

## Integration
---

* Command Output can be shown in the AWS Console, sent to **S3 bucket** or **CloudWatch Logs**
* **Send notifications to SNS about command status** (In progress, Success, Failed, …)
* Integrated with **IAM** & **CloudTrail**
* Can be invoked using **EventBridge**

# Patch Manager
---

* Automates the process of **patching managed instances**
	* OS updates, applications updates, security updates
	* Patch **on-demand** or on a schedule using Maintenance Windows
	* Can **scan instances** and **generate patch compliance report** (missing patches)

![[Pasted image 20230824191926.png]]

## Infrastructure Support
---

* Supports **EC2 instances** and **on-premises servers** 
* Supports **Linux, macOS, and Windows**

# Maintenance Windows
---

* **Defines a schedule** for when to perform actions on your instances
	* E.g. **OS patching**, **Updating drivers**, **Installing software**, …

![[Pasted image 20230824192400.png]]

## Settings
---

* **Schedule**
* **Duration** 
* **Set of registered instances** 
* **Set of registered tasks**

# Automation
---

* Simplifies **common maintenance and deployment tasks of EC2 instances and other AWS resources**, which can be triggered using:
	* Manually using **AWS Console, AWS CLI or SDK**
	* Amazon **EventBridge**
	* On a schedule using **Maintenance Windows**
	* By **AWS Config** for rules remediations
* Use Case Example: **Restart instances**, **Create an AMI, EBS snapshot**

![[Pasted image 20230824192619.png]]

## Automation Runbooks
---

* SSM Documents to **define actions preformed on your EC2 instances or AWS resources** (pre-defined or custom)