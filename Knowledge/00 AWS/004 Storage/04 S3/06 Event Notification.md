# What's Event Notification?
---

* Notify other AWS Services when S3 Events happens (E.g. **S3:ObjectCreated**, **S3:ObjectRemoved**, **S3:ObjectRestore**, **S3:Replication**…)
	* Can **filter object name** (E.g. *.jpg)

![[Pasted image 20230815021023.png]]

# Prerequisite: Provide Access to Events
---

## IAM Permission
---

![[Pasted image 20230815021156.png]]

# Via Amazon EventBridge
---

![[Pasted image 20230815021302.png]]

* **Advanced filtering options** with JSON rules (E.g. metadata, object size, name)
* **More Event Destinations** (E.g. Step Function, Kinesis Firehose...)
* **EventBridge Capabilities** – Archive, Replay Events, Reliable delivery