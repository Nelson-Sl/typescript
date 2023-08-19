# What's Athena?
---

* Serverless query service to **analyze data stored in Amazon S3**
	* Uses **standard SQL language** to query the files (built on Presto)
	* Supports **CSV, JSON, ORC, Avro, and Parquet**
	* Commonly used with **Amazon Quicksight** for reporting/dashboards

![[Pasted image 20230819140549.png]]

# Features: Federated Query
---

* Allows you to **run SQL queries across data stored in relational, non-relational, object, and custom data sources** (AWS or on-premises)
	* Uses **Data Source Connectors** that run on AWS Lambda
	* Store the results back in Amazon S3

![[Pasted image 20230819141056.png]]

# Performance Improvement
---

* Use **columnar data** for cost-savings (less scan, huge performance improvement)
	* E.g. **Apache Parquet** or **ORC** (Use [[06 Glue|Glue]] to convert to it)
* **Compress data** for smaller retrievals (bzip2, gzip, lz4, snappy, zlip, zstd…)
* **Partition datasets in S3** for easy querying on virtual columns
	* E.g. s3://athena-examples/flight/parquet/year=1991/month=1/day=1/
* **Use larger files** (> 128 MB) to minimize overhead
# Use Cases
---

* **Business intelligence / analytics / reporting**
* Analyze & query **VPC Flow Logs, ELB Logs, CloudTrail trails**, etc... (from S3)

# Pricing
---

* **$5.00 per TB of data scanned**

