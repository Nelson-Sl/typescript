# Security Options
---

* At-Rest Encryption (For **Master & Replicas** together) -> KMS Key
	* Note: To encrypt an un-encrypted database, should **go through a DB snapshot** and **restore it with encryption option**
* In-Flight Encyption -> TLS (Use **AWS TLS Root certificate** by client side)
* Authentication -> AWS **IAM Role** to connect to database
* Network Access/Authorization -> **Security group** to control the access to RDS/Aurora

# Note
---

1. **SSH is not Available** unless in RDS Custom mode
2. **Audit logs can be enabled** and send to cloudwatch for longer retention