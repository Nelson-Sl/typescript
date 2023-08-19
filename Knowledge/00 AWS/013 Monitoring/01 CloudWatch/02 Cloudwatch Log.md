# What consist of Cloudwatch log?
---

* Log groups
	* Arbitrary name, **usually representing an application**
* Log stream
	* **Instances within application / log files / containers**

# Log Source & Output

## Source
---

* The source of Cloudwatch log is coming from:
	* **SDK, CloudWatch Logs Agent, CloudWatch Unified Agent** 
	* **Elastic Beanstalk**: collection of logs from application 
	* **ECS**: collection from containers 
	* **AWS Lambda**: collection from function logs 
	* **VPC Flow Logs**: VPC specific logs 
	* **API Gateway** 
	* **CloudTrail** based on filter 
	* **Route53**: Log DNS queries

## Output
---

### Direct Export: S3
---

* Available to export data **within 12 hours** through **CreateExportTask** API

![[Pasted image 20230819194803.png]]

