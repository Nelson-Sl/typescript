# What's RedShift?
---

* It’s  a **OLAP** – online analytical processing (analytics and data warehousing) tool based on **PostgreSQL**
	* **Columnar storage of data** (instead of row based) & parallel query engine
	* **Has a SQL interface** for performing the queries
	* BI tools such as [[05 QuickSight|Amazon Quicksight]] or **Tableau integrate** with it

# How Redshift works?
---

* Leader node: for **query planning, results aggregation**
* Compute node: for **performing the queries, send results to leader**
	* Client **Provisioned the node size in advance** & Can **Use Reserved Instances** for cost savings

![[Pasted image 20230819142923.png]]

## Loading data to RedShift
---

![[Pasted image 20230819143235.png]]

# Backup
---

* Redshift **has “Multi-AZ” mode for some clusters** & **Need to restore the Snapshot of Redshift** in another AZ
	* Snapshots are **point-in-time backups** of a cluster, stored internally in S3
	* Mode
		* Automated: **Every 8 hours, every 5 GB, or on a schedule**. Set retention between **1 to 35 days**
		* Manual: snapshot **is retained until you delete it**

![[Pasted image 20230819143516.png]]

# Feature: Redshift Spectrum
---

* Query data that is already in S3 without loading it
	* Must have a **Redshift cluster available** to start the query, the query is then **submitted to thousands of Redshift Spectrum nodes**

![[Pasted image 20230819143907.png]]

# Performance
---

* **10x better performance** than other data warehouses, scale to PBs of data

# Payment
---

* Pay as you go **based on the instances provisioned**

# vs. [[01 Athena|Athena]]
---

* Faster queries / joins / aggregations thanks to indexes
* Good for **complicated queries**