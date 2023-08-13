# Simple Policy
---

* Route traffic to a single resource
	* Can specify same value **with multiple resource**. But **only the random one will chosen by client** if multiple values are returned
	* Can **only specify one AWS resource** when alias enabled
	* Can't be associated with [[08 Health Check|health check]]

![[Pasted image 20230813192402.png]]

# Weighted Policy
---

* Control the **% of requests that goes to each resource** ( **Calculated by Weight of a specific record / Sum of all weights for all records** )
	* DNS records must **have the same name and type**
	* **Assign a weight of 0 to a record** to stop sending traffic to a resource
	* If all records have weight of 0, **then all records will be returned equally**
	* Can't be associated with [[08 Health Check|health check]]

![[Pasted image 20230813193954.png]]

## Use Cases
---

* Load Balancing with different regions
* Testing new application version

# Latency Policy
---

* Redirect to the resource in specific AWS Region that **has the least latency close to us**
	* **Can be associated with [[08 Health Check|health check]] (has a failover capability)
	* Use Case: when **latency should be a priority in app**

![[Pasted image 20230813195802.png]]

# Failover Policy
---

* To route to the failover resource if [[08 Health Check|Health Check]] failed

![[Pasted image 20230813223804.png]]

# Geolocation Policy
---

* This will route to different resources based on **user location**
	* Specify location by **Continent**, **Country** or by **US State**
	* Should **create a “Default” record** in case there’s no match on location
	* Can be associated with [[08 Health Check|Health Check]]
* Use case
	* Website Localization
	* Restrict Content Distribution
	* Load Balancing

![[Pasted image 20230813224750.png]]

# GeoProximity Policy
---

* Route traffic to your resources **based on the geographic location of users and resources** & Ability to **shift more traffic to resources** based on the defined bias
	* To expand (1 to 99) – **more traffic to the resource**
	* To shrink (-1 to -99) – **less traffic to the resource**
* Prerequisite
	* Enable **Route 53 Traffic Flow**
* Support Resource
	* AWS Resource **specified with region**
	* Non-AWS Resource **specified with latitude and longitude**

![[Pasted image 20230813230049.png]]

![[Pasted image 20230813230107.png]]

# IP-Based Policy
---

* Routing to resource based on **clients’ IP addresses** ( E.g. from a specific ISP ) & Link **a list of CIDRs for clients** to corresponding **locations/endpoints** ( **IP-to-Endpoints** mapping )
* Use Case: **Optimize Performance**, **Reduce Cost**...

![[Pasted image 20230813233718.png]]

# Multi-value Policy
---

* Routing traffic to **multiple resources** so that it could **return multiple value / resources**
	* Up to **8** healthy records are returned for each Multi-Value query
	* Can be associated with Health Checks ( **return only values for healthy resources** )

![[Pasted image 20230813234333.png]]
