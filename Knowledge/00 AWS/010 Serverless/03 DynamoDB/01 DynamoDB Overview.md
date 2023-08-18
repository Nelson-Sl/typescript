# What's DynamoDB?
---

* An AWS managed, **NoSQL database** with **transaction support**
	* Has **Standard** & **Infrequent Access (IA)** Table Class
	* **Integrated with IAM** for security, authorization and administration

## Benefits
---

* **highly available** with **replication across multiple AZs**
* **Low cost** and **auto-scaling** capabilities
* **Fast and consistent in performance** (single-digit millisecond)
	* Scales to massive workloads, distributed database
	* Millions of requests per seconds, trillions of row, 100s of TB of storage

# How DynamoDB Works?
---

## Data Structure
---

* DynamoDB is made of **Tables**
* Each table **has a Primary Key** (must be decided at creation time)
* Each table can **have an infinite number of items (= rows)**
* Each item **has attributes (can be added over time – can be null)** -> Max size of Items is **400KB**