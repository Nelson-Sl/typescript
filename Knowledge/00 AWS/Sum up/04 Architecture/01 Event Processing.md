# SQS, SNS, Lambda
---

![[Pasted image 20230823212934.png]]

## Fan-Out Pattern
---

* To **deliver to multiple SQS**, we can **let multiple SQSes to subscribe SNS service**

![[Pasted image 20230823213057.png]]

# S3 Event Notification
---

## Option 1: Deliver to SQS, SNS & Lambda
---

* Can create as many “**S3 events**” as desired (E.g. **S3:ObjectCreated**, **S3:ObjectRemoved**, **S3:ObjectRestore**, **S3:Replication**…)
	* **Object name filtering possible** (*.jpg)
	* Typically **deliver events in seconds** but can **sometimes take a minute or longer**

![[Pasted image 20230823213541.png]]

# Option 2: EventBridge
---

* Advantage
	* **Advanced filtering options with JSON rules** (metadata, object size, name...)
	* **Multiple Destinations** – E.g. **Step Functions**, **Kinesis Streams / Firehose**…
	* **EventBridge Capabilities** – E.g. **Archive**, **Replay Events**, **Reliable delivery**

![[Pasted image 20230823213610.png]]

# Other Example
---

## Intercept API Calls: CloudTrail + EventBridge
---

![[Pasted image 20230823213852.png]]

## API Gateway + Kinesis Data Stream