# What's CloudFormation?
---

* A declarative way of **outlining your AWS Infrastructure**, for any resources (most of them are supported).
	* E.g. Security group, 2 EC2 instances using this security group, S3 bucket, Load balancer (ELB) in front of these machines
	* Creates those for you, **in the right order**, with the **exact configuration that you specify**

# Benefits
---

* **Infrastructure-as-Code**
	* **No resources are manually created**, which is excellent for control
	* Changes to the infrastructure **are reviewed through code**

* **Cost Estimate & Saving**
	* Each resources within the stack **is tagged with an identifier** so you can easily see how much a stack costs you. Also you can e**stimate the costs of your resources** using the CloudFormation template
	* Savings strategy: In Dev, you **could automation deletion of templates at 5 PM and recreated at 8 AM**, safely

* **Productivity** 
	* Ability to **destroy and re-create an infrastructure** on the cloud on the fly
	* **Automated generation of Diagram** for your templates -> [[01 CloudFormation#Cloudformation Stack Designer|Cloudformation Stack Designer]]
	* **Declarative programming** (no need to figure out ordering and orchestration)

* **No need to re-invent the wheel** 
	* Leverage existing templates on the web & documentation

* **Supports (almost) all AWS resources**
	* Everything we’ll see in this course is supported  & you can use “**custom resources**” for resources that are not supported

# Cloudformation Stack Designer
---

* Can **see all the resources** & **the relations between the components**

![[Pasted image 20230824150957.png]]
