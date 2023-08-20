# IAM Permission Boundaries
---

* IAM Permission Boundaries **are supported for users and roles** (not groups)
* Advanced feature to use a managed policy to **set the maximum permissions an IAM entity can get.**
	* Can be used in combinations of **AWS Organizations SCP**
* Use Cases
	* **Delegate responsibilities to non-administrators within their permission boundaries**, for example create new IAM users
	* Allow developers to **self-assign policies and manage their own permissions**, while making sure they can’t “escalate” their privileges (= make themselves admin)
 
![[Pasted image 20230820145157.png]]

# Policy Evaluation
---

![[Pasted image 20230820145713.png]]
