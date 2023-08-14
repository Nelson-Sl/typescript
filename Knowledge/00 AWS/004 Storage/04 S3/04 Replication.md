# Definition
---

* S3 Supports Cross-Region Replication (CRR) and Same-Region Replication (SRR) to **replicate the bucket object**
	* Process is **Asynchronous**
	* Can be **in different account**
	* Must **give proper IAM permissions to S3** & **Enable Versioning** for source & destination buckets

## Cross-Region Replication (CRR) 
---

* Support **Compliance**, **Low-latency access** & **Cross-account Replication**

## Same-Region Replication (SRR)
---

* Support **log aggregation**, **live replication** between test and production accounts

# Note
---

* By default **only new objects are replicated**. Can replicate existing objects or objects that fail to replicate using **S3 Batch Replication**
* For DELETE operations, it can **replicate delete markers** (optional) but **not able to replicate with a deletion with version ID**
* No **chaining** of operation, can only replicate the objects from the closest bucket