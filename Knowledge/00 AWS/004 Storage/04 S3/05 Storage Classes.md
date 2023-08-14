# S3 Standard
---

* General Purpose:  Used for **frequently accessed data** with low latency & high throughput
	* Use Case: **Big Data analytics**, **mobile & gaming applications**, **content distribution**…
* Infrequent Access (IA): For data that is **less frequently accessed, but requires rapid access when needed** (Lower Cost than GP)
		* Standard-IA: Disaster Recovery, backups
		* One-Zone IA: **data lost when AZ is destroyed** & Lower Availability, Use for Storing **secondary backup copies of on-premises data**, or data you can **recreate**


# Glacier
---

* **Low-cost object storage** meant for **archiving / backup**, Pay for **cost for storage + object retrieval**
	* **Instant Retrieval**: storage duration >= 90 days, 