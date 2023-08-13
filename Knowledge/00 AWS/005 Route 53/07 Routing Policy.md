# Simple Policy
---

* Route traffic to a single resource
	* Can specify same value **with multiple resource**. But **only the random one will chosen by client** if multiple values are returned
	* Can **only specify one AWS resource** when alias enabled
	* Can't be associated with health check

![[Pasted image 20230813192402.png]]

# Weighted Policy
---

* Control the **% of requests that goes to each resource** ( **Calculated by Weight of a specific record / Sum of all weights for all records** )
	* DNS records must **have the same name and type**
	* **Assign a weight of 0 to a record** to stop sending traffic to a resource
	* If all records have weight of 0, **then all records will be returned equally**
	* Can't be associated with health check

![[Pasted image 20230813193954.png]]

## Use Cases
---

* Load Balancing with different regions
* Testing new application version