# Definition
---

Route 53 provide HTTP health check for **public resources**. 

# How to do Health Check?
---

## Monitor Endpoint
---

* About **15 global health checkers** will check the endpoint health, can support HTTP, HTTPS & TCP following configurations:
	* **Healthy/Unhealthy Threshold** – ( **by default 3** )
	* **Interval** – 30 sec (can set to 10 sec – higher cost)
	* can be setup to pass / fail **based on the text in the first 5120 bytes of the response**
	* choose **which locations you want Route 53 to use**
* To Pass the endpoint:
	* Health Checks pass only when the endpoint **responds with the 2xx and 3xx status codes**
	* If **> 18%** of health checkers report the endpoint is healthy, Route 53 considers it Healthy. Otherwise, it’s Unhealthy

![[Pasted image 20230813215817.png]]
