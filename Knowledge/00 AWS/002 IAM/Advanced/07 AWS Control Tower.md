# What's AWS Control Tower?
---

* Easy way to **set up and govern a secure and compliant multi-account AWS environment** based on best practices
	* Use [[01 Organization|AWS Organization]] to create account

# Security: Guardrails
---

* Provides **ongoing governance for your Control Tower environment** (AWS Accounts)
	* **Preventive Guardrail** – using [[01 Organization#Security Service Control Policies (SCP)|SCPs]] (e.g., Restrict Regions across all your accounts)
	* **Detective Guardrail** - using [[00 AWS/013 Monitoring/03 AWS Config/01 Overview|AWS Config]] (e.g., identify untagged resources)

![[Pasted image 20230820162520.png]]

# Benefits
---

* Automate the **set up of your environment in a few clicks**
* Automate ongoing policy management using [[07 AWS Control Tower#Security Guardrails|guardrails]]
• **Detect policy violations** and remediate them
• **Monitor compliance** through an interactive dashboard
