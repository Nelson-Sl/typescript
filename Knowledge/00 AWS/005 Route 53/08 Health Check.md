# Definition
---

Route 53 provide HTTP health check for **public resources**. 

# How to do Health Check?
---

## Monitor Endpoint
---

* About **15 global health checkers** will check the endpoint health, with following configurations:
	* **Healthy/Unhealthy Threshold** – ( **by default 3** )
	* **Interval** – 30 sec (can set to 10 sec – higher cost)

![[Pasted image 20230813215817.png]]
