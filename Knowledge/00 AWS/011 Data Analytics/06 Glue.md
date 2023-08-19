# What's Glue?
---

* Serverless service & managed **extract, transform, and load (ETL) service** that  useful to **prepare and transform data for analytics**

![[Pasted image 20230819152638.png]]

# Features
---

# Glue Data Catalog: catalog of datasets
---

![[Pasted image 20230819152844.png]]

# Other Features
---

* Glue Job Bookmarks: prevent **re-processing old data**
* Glue Elastic Views:
	* Combine and replicate data across multiple data stores using SQL • No custom code, Glue monitors for changes in the source data, serverless • Leverages a “virtual table” (materialized view)
* Glue DataBrew: **clean and normalize data using pre-built transformation**
* Glue Studio: new **GUI** to create, run and monitor ETL jobs in Glue
* Glue Streaming ETL (built on Apache Spark Structured Streaming): **compatible with Kinesis Data Streaming, Kafka, MSK** (managed Kafka)
# Use Case: Convert data into Parquet format
---

![[Pasted image 20230819152720.png]]
