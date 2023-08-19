# What is EMR?
---

* helps creating **Hadoop clusters (Big Data)** to analyze and process vast amount of data, which can be made of **hundreds of EC2 instances**
	* EMR bundled with **Apache Spark, HBase, Presto, Flink**…but take care of **all the provisioning and configuration**
	* **Auto-Scaling**

# Node Types
---

* Master Node
	* Manage the cluster, coordinate, manage health – **long running**
* Core Node
	* Run tasks and store data – **long running**
* Task Node (Optional)
	* Just to run tasks – transient & usually **Spot**

# Purchasing Options
---

* **On-Demand**
	* reliable, predictable, won’t be terminated
* Reserved (min 1 year)
	* **cost savings** (EMR will automatically use if available)
* Spot
	* cheaper, can be terminated, less reliable

# Use Case
---

* **data processing**, **machine learning**, **web indexing**, **big data**…