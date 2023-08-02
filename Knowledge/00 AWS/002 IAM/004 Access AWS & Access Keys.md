# Option to Access AWS
---

* AWS Management Console
	* Visit through **Web Browser**, protected by [[003 Security with Password & MFA | Password & MFA]]
* AWS Command Line Interface (CLI)
	* Visit through **commands in command-line shell**, protected by [[004 Access AWS & Access Keys#Access Keys | Access Keys]]
	* E.g. `aws s3 ls s3://my-bucket`
	* CLI Cloud Version: **AWS Cloudshell** 
* AWS Software Development Kit (SDK)
	* **Set of Language-Specific APIs** (or libraries)
	* Embedded within application & Visit through **application code**, protected by [[004 Access AWS & Access Keys#Access Keys | Access Keys]]
	* Support Language
		* SDKs: Java, JavaScript, Go, Ruby, Node.js, C++, Python, PHP, .NET
		* Mobile: Android, iOS...
		* IoT Devices: Embedded C, Arduino

# Access Keys
---
Another AWS Secrets that generated through the AWS console, and used to protect AWS root & IAM account through **CLI** and **SDK**.

Components:
* Access Key ID: Work as **Username**
* Secret Access Key: Work as **Password**
