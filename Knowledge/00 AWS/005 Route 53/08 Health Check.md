# Definition
---

Route 53 provide HTTP health check for **public resources**. 

# How to do Health Check?
---

## Monitor Endpoint
---

* About **15 global health checkers** will check the endpoint health, can support **HTTP, HTTPS & TCP** with following configurations:
	* **Healthy/Unhealthy Threshold** – ( **by default 3** )
	* **Interval** – 30 sec (can set to 10 sec – higher cost)
	* can be setup to pass / fail **based on the text in the first 5120 bytes of the response**
	* choose **which locations you want Route 53 to use**
* To Pass the endpoint:
	* Health Checks pass only when the endpoint **responds with the 2xx and 3xx status codes**
	* If **> 18%** of health checkers report the endpoint is healthy, Route 53 considers it Healthy. Otherwise, it’s Unhealthy
* Note:
	* Configure you **router/firewall** to allow incoming requests from Route 53 Health Checkers

![[Pasted image 20230813215817.png]]

## Calculated Health Checks
---

* Combine the results of multiple Health Checks **into a single Health Check**, with following configurations:
	* Use **OR, AND or NOT**
	* Specify **how many of the health checks need to pass** to make the parent pass ( **up to 256** )
* Use Case: perform maintenance to your website **without causing all health checks to fail**

![[Pasted image 20230813222000.png]]

## HC For Private Hosted Zones / Private Resource
---

