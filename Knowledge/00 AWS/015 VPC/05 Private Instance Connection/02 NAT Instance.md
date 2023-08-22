# How NAT Instance Works?
---

* NAT stands for **Network Address Translation**, which allows **EC2 instances in private subnets to connect to the Internet**
* NAT Instance is an instance **launched in public subnets** that functioned as NAT. To achieve this functionality it should:
	* Must disable EC2 **Source / destination Check**
	* Must have **Elastic IP attached to it**
	* **Route Tables must be configured** to route traffic from private subnets to the NAT Instance

![[Pasted image 20230822084843.png]]

![[Pasted image 20230822085354.png]]

# Notes & Requirements
---

* **Pre-configured Amazon Linux AMI** is available 
	* Reached the end of standard support on December 31, 2020
* • Internet traffic bandwidth **depends on EC2 instance type**