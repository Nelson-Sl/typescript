	* Root Account / User / Groups
	* Don't use the [[001 Introduction#Root Account | root account]] except for AWS account setup (Use IAM Account)
	* 1 Physical user = 1 AWS User
	* Assign users to groups, as well as permissions
	* Create and use roles for giving permissions to AWS Services
* Group / User Security
	* Use & Enforce the use of [[003 Security with Password & MFA#Multi-Factor Authentication (MFA)|MFA]]
	* Use [[004 Access AWS & Access Keys#Access Keys|Access Keys]] for Programatic Access (CLI/SDK)
	* **Never** share IAM User & Access Keys
* Audit / Report
	* Audit your account's permissions through [[005 Security Tools#IAM Credentials Report|IAM Credentials Report]] and [[005 Security Tools#IAM Access Advisor|IAM Access Advisor]] 