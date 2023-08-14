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
	* **Instant Retrieval**: storage duration >= **90** days, Millisecond Retrieval
	* **Flexible Retrieval**: storage duration >= **90** days, can be retrieved on Expedited (1-5 minutes), Standard (3 to 5 hours), Bulk (5 to 12 hours)
	* **Deep Archive**: storage duration >= **180** days, can be retrieved on Standard (12 hours), Bulk (48 hours)

# Intelligent-Tiering
---

* Moves objects **automatically between Access Tiers based on usage**, no **retrieval charges** but **should pay for auto-tiering & monitoring**
	* **Frequent Access tier** (automatic): default tier 
	* **Infrequent Access tier** (automatic): objects not accessed for 30 days 
	* **Archive Instant Access tier** (automatic): objects not accessed for 90 days 
	* **Archive Access tier** (optional): configurable from 90 days to 700+ days 
	* **Deep Archive Access tier** (optional): config. from 180 days to 700+ days

# Comparisons
---

![[Pasted image 20230814222955.png]]

![[Pasted image 20230814223019.png]]

# Moving Storage Classes: Lifecycle Policy
---

* Automated moving storage classes processes (for a **certain object prefix or tag**)
	* **Transition Actions** – configure objects to transition to another storage class
		* E.g. **Move objects to Standard IA class** 60 days after creation
	* **Expiration actions** – configure objects to expire (delete) after some time
		* Access log files can be set to delete after a 365 days
		* Delete **Older version of files** or **files that failed for multi-upload**

## Support Tools: Amazon S3 Analytics
---

* Help you decide **when to transition objects to the right storage class** (Only available for **standard** and **standard IA**)
	* Report **starts in 24-48 hour** and **is updated daily**