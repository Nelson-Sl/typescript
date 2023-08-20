# What is Docker?
---

* Docker is a software development platform to **deploy apps**, where they will be **packaged in Containers**.
	* Can **run in any machine** (No compatibility issue)
	* Works with **any language, any OS, any technology**
	* **Easy to maintain & Deploy,** Predictable Behavior
	* Less Work

![[Pasted image 20230817112925.png]]\

## Storage
---

* Docker Images stores in Docker Repositories. Some Examples might be:
	* **Docker Hub** (https://hub.docker.com) or **Amazon ECR Public Gallery** https://gallery.ecr.aws
		* Public repository 
		* Find base images for many technologies or OS (e.g., **Ubuntu, MySQL, …**)
	* **Amazon ECR (Amazon Elastic Container Registry)** 
		* Private repository

# vs Virtual Machines
---

* Resources **are shared with the host** => many containers on one server

![[Pasted image 20230817113742.png]]

# How Does Docker Work?
---

![[Pasted image 20230817113426.png]]

# AWS Container Infrastructure
---

* [[01 AWS ECS (Elastic Container Service)|Amazon Elastic Container Service (Amazon ECS)]]  -> **Amazon’s own container platform**
* [[04 Elastic Kubernetes Service (EKS)|Amazon Elastic Kubernetes Service (Amazon EKS)]] -> **Amazon’s managed Kubernetes (open source)**
* [[01 AWS ECS (Elastic Container Service)#Fargate Launch Type|AWS Fargate]] -> **Amazon’s own Serverless container platform**
	* Works with ECS & EKS
* [[03 ECR (Elastic Container Registry)|Amazon ECR]] -> **Store container images**
