This section is associated with [[002 Policies|IAM Policies]]

# Restrict Client IP
---

![[Pasted image 20230820140950.png]]

# Restrict By Requested Region
---

![[Pasted image 20230820141033.png]]

# Restrict By Resource Tag
---

![[Pasted image 20230820141125.png]]

# Force MFA
---

![[Pasted image 20230820141213.png]]

# S3 Restriction Policies
---

* Bucket Level Permission
	* **s3:ListBucket** permission applies to arn:aws:s3:::test
* Object level permission
	* **s3:GetObject, s3:PutObject, s3:DeleteObject** applies to arn:awn:s3:::test/*

![[Pasted image 20230820141658.png]]

# Restrict Organizational Members
---

* aws:PrincipalOrgID can be used in any resource policies to restrict access to accounts **that are member of an AWS Organization**

![[Pasted image 20230820141701.png]]
