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
	* Each resources within the stack **is tagged with an identifier** so you can easily see how much a stack costs you . You can estimate the costs of your resources using the CloudFormation template