# What is S3?
---

Amazon S3 allows people to store objects (files) in [[01 Overview#Buckets|Buckets]] (directories)

## Buckets
---

* **Defined at the region level** & must **have a globally unique name** (across all regions & all accounts)
* Naming Convention
	* No **UpperCase & Underscore**
	* Must start with a **lowercase letter** or **number**
	* **3-63** characters long
	* **Not an IP**
	* Not start with prefix **xn--** or end with suffix **-s3alias**

## Objects
---

* Object in S3 bucket contains:
	* **Key with full path** (prefix + object name) 
		* E.g. s3://my-bucket/**my_folder1/another_folder/my_file.txt**
	* **Values**
		* Max Object Size **5TB**
		* Multi-part upload if **upload > 5GB**
	* **Metadata** (list of text key / value pairs – system or user metadata)
	* **Tags** (Unicode key / value pair – up to 10) – useful for security / lifecycle
	* **Version ID** (if versioning is enabled)

# S3 Use Cases
---

* Backup and storage 
* Disaster Recovery 
* Archive 
* Hybrid Cloud storage 
* Application hosting 
* Media hosting 
* Data lakes & big data analytics 
* Software delivery 
* Static website