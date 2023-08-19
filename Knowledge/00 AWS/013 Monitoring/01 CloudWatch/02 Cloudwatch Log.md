# What consist of Cloudwatch log?
---

* Log groups
	* Arbitrary name, **usually representing an application**
* Log stream
	* **Instances within application / log files / containers**

# Log Source & Output
---

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
* **Not near-real time or real-time…** use Logs Subscriptions instead

![[Pasted image 20230819194803.png]]

### Logs Subscriptions
---

* Get a **real-time log events from CloudWatch Logs** for processing and analysis
* **Destination**
	* Kinesis Data Stream (Can be **cross-account** & **cross-region**)
	* Kinesis Data Firehose (Can be **cross-account** & **cross-region**)
	* Lambda
	* OpenSearch
* **Subscription Filter** – filter which logs are events delivered to your destination

![[Pasted image 20230819195306.png]]

![[Pasted image 20230819195521.png]]

![[Pasted image 20230819195553.png]]

# Security
---

* Logs are **encrypted by default** & Can **setup KMS-based encryption with your own keys**

# Feat