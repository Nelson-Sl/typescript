# What's RedShift?
---

* It’s  a **OLAP** – online analytical processing (analytics and data warehousing) tool based on **PostgreSQL**
	* **Columnar storage of data** (instead of row based) & parallel query engine
	* **Has a SQL interface** for performing the queries
	* BI tools such as **Amazon Quicksight** or **Tableau integrate** with it

# How Redshift works?
---

* Leader node: for **query planning, results aggregation**
* Compute node: for **performing the queries, send results to leader**
	* Client **Provisioned the node size in advance** & Can **Use Reserved Instances** for cost savings

![[Pasted image 20230819142923.png]]

# Performance
---

* **10x better performance** than other data warehouses, scale to PBs of data

# Payment
---

* Pay as you go **based on the instances provisioned**