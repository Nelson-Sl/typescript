# What's Amazon Cognito?
---

* Give users an identity to interact **with our web or mobile application**

# How Amazon Cognito Works?
---

## Cognito User Pools
---

* A **sign in functionality for app users** that **create a serverless database of user** for your web & mobile apps
	* Integrate with **API Gateway** & **Application Load Balancer**
	* Service
		* **Simple login**: Username (or email) / password combination & **Password Reset**
		* **Email & Phone Number Verification**
		* **Multi-factor authentication (MFA)**
		* Federated Identities: users from **Facebook, Google, SAML**…

![[Pasted image 20230818160643.png]]

## Cognito Identity Pools
---

* A service for Federated Identities (E.g. users from **Facebook**) to get identities for “users” so **they obtain temporary AWS credentials**
	* Source can be Get identities for “users” so **they obtain temporary AWS credentials**
	* If validated, users can then access AWS services **directly or through API Gateway**

![[Pasted image 20230818160935.png]]

### Access & Authorization Control
---

* The **IAM policies applied to the credentials** are defined in Cognito
	* **Default IAM roles** for authenticated and guest users
	* They can be customized based on the user_id for fine grained control (till **Row Level**)

![[Pasted image 20230818161337.png]]
