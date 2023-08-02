# What is Auto Scaling Group (ASG) ?
---

Auto Scaling Group (ASG) is a free AWS Service that aims to:
* **Scale out (add EC2 instances)** to match an increased load **till maximum capacity**
* **Scale in (remove EC2 instances)** to match a decreased load **till minimum capacity**
* **Re-create an EC2 instance** in case a previous one is terminated (ex: if unhealthy)
![[asg.png]]

# Co-Work Services
---

## Load Balancer
---

ASG can **automatically register a load balancer** to new instances
![[asg_with_load_balancer.png]]

## Cloudwatch
---

It's possible to scale in or scale out ASG **based on the cloudwatch alarms & metrics** (E.g. Average CPU, Custom Metrics)
![[asg_cloudwatch.png]]

# How to Create ASG?
---

* **Launch Template**
	* AMI + Instance Type
	* EBS Volumes
	* Security Group
	* SSH Key Pair
	* IAM Roles for EC2 Instance
	* Network + Subnet Information
	* Load Balancer Information
	* EC2 User Data
* **Minimum / Maximum / Initial Capacity**
* Scaling Policy