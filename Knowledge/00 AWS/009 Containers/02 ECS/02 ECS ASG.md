# EC2 Launch Type
---

* Auto Scaling Group Scaling
	* Scale your ASG based on **CPU Utilization** & **Add EC2 instances over time**
* ECS Cluster Capacity Provider
	* Used to automatically provision and scale the infrastructure for your ECS Tasks
	* Work with ASG & Add EC2 Instances when you’re missing capacity (**CPU, RAM…**)

![[Pasted image 20230817182713.png]]

# Fargate Launch Type
---

* **Automatically increase/decrease the desired number of ECS tasks** (Much easier than EC2)
* Uses **AWS Application Auto Scaling**
	* Metrics
		* ECS Service **Average CPU Utilization**
		* ECS Service **Average Memory Utilization** - Scale on RAM
		* **ALB Request Count Per Target** – metric coming from the ALB
	* Scaling Method
		* Target Tracking – scale based on **target value for a specific CloudWatch metric**
		* Step Scaling – scale **based on a specified CloudWatch Alarm**
		* Scheduled Scaling – scale based **on a specified date/time** (predictable changes)