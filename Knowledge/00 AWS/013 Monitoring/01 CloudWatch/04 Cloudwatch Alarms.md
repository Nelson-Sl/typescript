# What's CloudWatch Alarm?
---

* Alarms are used to **trigger notifications for any metric**
	* Note: can be created based on **CloudWatch Logs Metrics Filters**
	* Can be tested by **setting the alarm state in CLI**
		* aws cloudwatch set-alarm-state --alarm-name "myalarm" --state-value ALARM --state-reason "testing purposes"

![[Pasted image 20230819203051.png]]

## Composite Alarm
---

* Composite Alarms **are monitoring the states of multiple other alarms** (AND or OR)
* Helpful to **reduce “alarm noise”** by creating complex composite alarms

![[Pasted image 20230819203512.png]]
	
# CloudWatch Alarm Attributes
---

* Alarm States: **OK**, **INSUFFICIENT_DATA**, **ALARM**
* Period: **Length of time in seconds to evaluate the metric** (E.g. 10 sec, 30 sec or multiples of 60 sec)
* Threshold: 
	* E.g. **sampling, %, max, min**, etc…

# CloudWatch Alarm Target
---

## Stop, Terminate, Reboot, or Recover an EC2 Instance
---

![[Pasted image 20230819203729.png]]

# Other
---

* Trigger **Auto Scaling Action**
* **Send notification to SNS** (from which you can do pretty much anything)