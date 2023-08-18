# RDBMS (= SQL / OLTP)
---

* RDS, Aurora
	* Store **relational datasets (RDBMS / OLTP)**, perform **SQL queries, transactions**
		* Great for JOIN Queries
	* Aurora **Cost 20% higher**, but with **less maintenance / more flexibility / more performance / more features**


# NoSQL Database
---

## ElasticCache: Key/Value Pair
---

* **Frequent Read But Less Writes**
	* cache **results for DB queries**
	* **store session data** for websites
* Can't use SQL & Need Application Change

## DynamoDB
---

* Distributed serverless cache
	* Can replace ElastiCache as a key/value store (storing session data for example, using TTL feature), **distributed but slight lower performance**
* Serverless applications development (**small documents** 100s KB)
* Great for application to **rapidly evolve schemas**

# Object Store: S3 / Glacier
---

* S3
	* store **static files**
	* key value store for **big files**
	* **Media / Website hosting**
	* **Archive Files**
* Glacier
	* **Archive Files**