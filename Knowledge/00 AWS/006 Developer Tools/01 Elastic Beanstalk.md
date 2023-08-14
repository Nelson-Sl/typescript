# What's Elastic Beanstalk
---

* Elastic Beanstalk is **a developer centric view of deploying an application on AWS**
	* It's a **managed service** and developer only takes in charge of application code. AWS automatically handles capacity provisioning, load balancing, scaling, application health monitoring, instance configuration, etc.
	* It uses all the component’s we’ve seen before: **EC2, ASG, ELB, RDS, …**

# How Elastic Beanstalk works?
---

* Application: collection of **Elastic Beanstalk components** (environments, versions, configurations, …) 

![[Pasted image 20230814201016.png]]

# Charge
---

* Beanstalk is **free** but will **pay for the underlying instances**