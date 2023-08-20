# What's an Organization?
---

* A Global service that **allows to manage multiple AWS accounts**

# How does Organization Works?
---

* The main account is the **management account**, other accounts are **member accounts**

![[Pasted image 20230820134542.png]]

![[Pasted image 20230820134609.png]]

# Advantages
---

* **Multi Account** vs One Account Multi VPC
* Use **tagging standards** for billing purposes
* **Enable CloudTrail on all accounts**, **send logs to central S3 account**
* Send CloudWatch Logs to **central logging account**
* Establish **Cross Account Roles** for Admin purposes -> Service Control Policies (SCP)
* API is available to **automate AWS account creation** 

# Security: Service Control Policies (SCP)
---

* IAM policies applied to OU or Accounts to **restrict Users and Roles** and do **not apply to the management account** (full admin power)
* **Must have an explicit allow** (does not allow anything by default – like IAM)

![[Pasted image 20230820140049.png]]

![[Pasted image 20230820140114.png]]

# Pricing
---

* **Consolidated Billing** across all accounts - single payment method
* Pricing benefits **from aggregated usage** (volume discount for EC2, S3…)
* Shared **reserved instances** and **Savings Plans discounts** across accounts