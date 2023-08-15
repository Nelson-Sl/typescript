# S3 & Glacier Select
---

* Retrieve less data using **Simple SQL** by **performing server-side filtering** (Can filter **rows & columns**)
	* Less **Network Transfer & CPU Cost** at client side
	* Up to **400% faster** & **80% cheaper**

![[Pasted image 20230815023154.png]]

# Batch Operations
---

* S3 Inventory to **get object list** -> use S3 Select to **filter your objects** -> **Perform bulk operations on existing S3 objects** with a single request
	* E.g. Modify object metadata & properties, Copy objects between S3 buckets, **Encrypt un-encrypted objects**, Modify ACLs & tags, Restore objects from S3 Glacier, Invoke Lambda function
	* manages **retries**, **tracks progress**, **sends completion notifications**, **generate reports**

![[Pasted image 20230815024024.png]]
