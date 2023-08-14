* EC2 Instance
	* **Use Golden AMI** (Install your applications, OS dependencies etc.. **beforehand** and launch your EC2 instance from the Golden AMI)
	* **Bootstrap Using user Data**: use **User Data Script** to allow dynamic configuration
	* **Hybrid**: Use Elastic Beanstalk to apply both Golden AMI & Boostrap
* RDS Database & EBS Volume
	* **Restore from the snapshot** to get format/schema and data ready