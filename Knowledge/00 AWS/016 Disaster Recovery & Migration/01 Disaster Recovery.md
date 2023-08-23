# What's Disaster Recovery?
---

* Disaster recovery (DR) is about preparing for and recovering from a **disaster**, or any event that **has a negative impact on a company’s business continuity or finances**
	* On-premise => On-premise: **traditional DR, and very expensive**
	* On-premise => AWS Cloud: **hybrid recovery**
	* AWS Cloud Region A => AWS Cloud Region B

# Disaster Recovery Strategy
---

## Evaluation Term
---

* Recovery point objective (RPO)
	* the maximum amount of data – as measured by time – **that can be lost after a recovery from a disaster, failure, or comparable event** before data loss will exceed what is acceptable to an organization.
* Recovery time objective (RTO)
	* The **duration of time and a service level** within which a **business process must be restored after a disaster in order to avoid unacceptable consequences associated with a break in continuity.**

![[Pasted image 20230823170700.png]]

## Backup & Restore 
---

* High **RPO** & **Slower RTO**

![[Pasted image 20230823170828.png]]

## Pilot Light
---

* Very similar to Backup and Restore but **a small version of the app is always running in the cloud**
	* Faster than Backup and Restore as **critical systems are already up**

![[Pasted image 20230823171142.png]]

## Warm Standby
---

* Full system is up and running, but **at minimum size**
* Upon disaster, we can **scale to production load**

![[Pasted image 20230823171334.png]]

## Multi Site / Hot Site Approach
---

* Full Production Scale is running **AWS** and **On Premise**
* **Very low RTO** (minutes or seconds) – very expensive

![[Pasted image 20230823172048.png]]

## All AWS Region
---

![[Pasted image 20230823172141.png]]

# Disaster Recovery Tips
---

* Backup 
	* **EBS Snapshots**, **RDS automated backups** **/ Snapshots**, etc… 
	* Regular pushes to **S3 / S3 IA / Glacier, Lifecycle Policy, Cross Region Replication** 
	* From On-Premise: Snowball or Storage Gateway 
* High Availability 
	* Use **Route53** to migrate DNS over from Region to Region 
	* **RDS Multi-AZ**, **ElastiCache Multi-AZ**, **EFS**, **S3** 
	* **Site to Site VPN** as a recovery from Direct Connect 
* Replication 
	* **RDS Replication** (Cross Region), **AWS Aurora + Global Databases** 
	* Database replication from on-premises to RDS 
	* **Storage Gateway** 
* Automation 
	* CloudFormation / Elastic Beanstalk to re-create a whole new environment
	* Recover / Reboot EC2 instances with CloudWatch if alarms fail 
	* AWS Lambda functions for customized automations 
* Chaos 
	* Netflix has a “simian-army” randomly terminating EC2