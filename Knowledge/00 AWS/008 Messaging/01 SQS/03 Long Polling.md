# What's Long Polling
---

* The time **consumer “wait” for messages to arrive** if there are none in the queue
	* **1-20 sec** (20 sec / Longer Polling is Preferable)
	* Can be enabled at Queue level or through **WaitTimeSeconds API**

# Benefit
---

*  LongPolling **decreases the number of API calls made to SQ**S while **increasing the efficiency and reducing latency of your application**