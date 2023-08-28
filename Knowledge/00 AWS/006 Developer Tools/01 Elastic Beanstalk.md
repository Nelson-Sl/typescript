``# What's Elastic Beanstalk
---

* Elastic Beanstalk is **a developer centric view of deploying an application on AWS**
	* It's a **managed service** and developer only takes in charge of application code. AWS automatically handles capacity provisioning, load balancing, scaling, application health monitoring, instance configuration, etc.
	* It uses all the component’s we’ve seen before: **EC2, ASG, ELB, RDS, …**
	* Have **full control over configuration**

# How Elastic Beanstalk works?
---

* **Application**: collection of **Elastic Beanstalk components** (environments, versions, configurations, …) 
* **Application Version**: an iteration of **your application code**
* **Environment**: **Collection of AWS resources** running an application version (only one application version at a time)
	* Can **have multiple environments** (dev, test, sit...)
	* Tier
		* **Web Server Tier** (Working with ELB)
		* **Worker Tier** (Scale **based on the number of SQS Messages**, can **push message from web server tier**)

![[Pasted image 20230814201016.png]]

![[Pasted image 20230814201526.png]]

# Deployment Modes
---

![[Pasted image 20230814202011.png]]


# Supported Platforms
---

![[Pasted image 20230814201903.png]]


# Charge
---

* Beanstalk is **free** but will **pay for the underlying instances**