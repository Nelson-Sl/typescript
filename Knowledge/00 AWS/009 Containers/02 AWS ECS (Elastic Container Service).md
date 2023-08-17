# How AWS ECS Works?
---

* **Launch ECS Tasks on ECS Clusters** (Similar to Launch Docker containers on AWS)

## EC2 Launch Type
---

* Each EC2 Instance **must run the ECS Agent to register in the ECS Cluster**
* Clients must **provision & maintain the infrastructure** (the EC2 instances)

![[Pasted image 20230817171405.png]]

## Fargate Launch Type
---

* **Create task definitions** & AWS just **runs ECS Tasks for you based on the CPU / RAM you need**
* **All Serverless** & **Do not provision the infrastructure** (no EC2 instances to manage)
* **Automatic Scaling**: Scale based on the number of tasks

![[Pasted image 20230817172559.png]]

# Access Control: IAM Roles
---

* EC2 Instance Profile
	* Only **Required by EC2 Launch Type** & Used by **EC2 Agent** to access other service
		* E.g. **Makes API calls to ECS service**, **Send container logs to CloudWatch Logs**,  **Pull Docker image from ECR**, **Reference sensitive data in Secrets Manager or SSM Parameter Store**
* EC2 Task Role
	* Defined in **task definition**
	* Use **different roles for the different ECS Services** to access other service

![[Pasted image 20230817173713.png]]

# Integration with Other Service
---

## Load Balancer
---

* **Application Load Balancer (ALB)**: Support Most Use Cases
* **Network Load Balancer (NLB)**: recommended only for **high throughput / high performance use cases**, or to **pair it with AWS Private Link**
* **Classic Load Balancer (CLB)**: Not Support Fargate

 ![[Pasted image 20230817175412.png]]

## Data Volume (EFS)
---

