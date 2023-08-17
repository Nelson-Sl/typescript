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

* create task definitions 

![[Pasted image 20230817172559.png]]
