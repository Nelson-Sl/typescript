# What is Metrics in Cloudwatch?
---

* Metric is **a variable to monitor for every services in AWS** 
	* E.g. **CPUUtilization**, **NetworkIn**…

# What belongs to Metrics / What metrics include
---

* Metrics belong to **namespaces**
* Metrics have
	* **Timestamp**
	* Dimension 
		* **an attribute of a metric** (instance id, environment, etc…)
		* **Up to 30 dimensions** per metric

# Category of Metrics
---

* CloudWatch **dashboards of metrics**
* CloudWatch **Custom Metrics** (E.g. RAM)

# CloudWatch Metric Streams
---

* Continually stream CloudWatch metrics **to a destination of your choice**, with **near-real-time delivery** and low latency.
	* E.g. **Amazon Kinesis Data Firehose** & **3rd party service provider** (Datadog, Dynatrace, New Relic, Splunk, Sumo Logic…)
* Option to **filter metrics to only stream a subset of them**

![[Pasted image 20230819192837.png]]
