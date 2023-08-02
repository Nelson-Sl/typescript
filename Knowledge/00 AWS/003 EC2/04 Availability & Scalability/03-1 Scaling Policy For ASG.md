# Dynamic Scaling Policies
---
* **Target Tracking Scaling**
	* E.g. I want the average ASG CPU to stay around 40%
* **Simple Step Scaling**
	* E.g. When a CloudWatch alarm is triggered (example CPU > 70%), then add 2 units
	* Suggested Scale-On Metrics: **CPUUtilization**, **ResourceCountPerTarget**, **Average Network In/Out**, Custom Metrics
* **Scheduled Actions** (Based on known usage patterns)
	* E.g. Increase the min capacity to 10 at 5 pm on Fridays

# Predictive Scaling Policies
---
Continuously **forecast load** and schedule scaling ahead 
![[predictive_scaling.png]]

# Scaling Cooldowns
---
* Definition: **The cooldown period** after a scaling action happens (Default **300** seconds). During this time ASG won't launch or terminate additional instances to allow the scaled instance to stabilitize.
* Suggestion: **Use a ready-to-use AMI** to reduce configuration time & cooldown period