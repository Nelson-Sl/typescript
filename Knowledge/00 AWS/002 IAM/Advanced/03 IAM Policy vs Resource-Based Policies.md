# Difference
---

* When you assume an IAM role (user, application or service), you **give up your original permissions** and **take the permissions assigned to the role**
* When using a resource-based policy, the principal **doesn’t have to give up his permissions**

# Example: Amazon EventBridge Permission
---

* When a rule runs, it **needs permissions on the target**
* Resource-based policy: **Lambda, SNS, SQS, CloudWatch Logs, API Gateway**…
* IAM role: **Kinesis stream, Systems Manager Run Command, ECS task**…

![[Pasted image 20230820143059.png]]
