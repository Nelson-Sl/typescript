## IAM Concept
---
IAM stands for **Identity and Account Management**, it's a **Global** Service

## Key Concepts for IAM
---

### Root Account
---
 
 Default AWS Account, couldn't be shared or used
 
### Users
---

Mapped to a physical user to organization and have the password to log in to console

### Groups
---

Department/Group in organizations, consists of users
* **Note:** Users could be **in no groups** or **in several groups**

### Policies
---

JSON documents that defines the permissions **for users and groups** ^iampolicy

### Roles
---

JSON documents that defines the permissions **for special AWS services to perform special AWS actions**
* Examples
	* **EC2 Instance** Roles
	* **Lambda Function** Roles
	* **Cloudformation** Roles


