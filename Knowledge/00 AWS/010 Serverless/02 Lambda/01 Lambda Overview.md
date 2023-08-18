# Benefits of Lambda
---

* [[01 Lambda Overview#Pricing|Easy & Cheap Pricing]]
* [[01 Lambda Overview#Integrated Service|Integrated with the whole AWS suite of services]]
* [[01 Lambda Overview#Language Support|Integrated with many programming languages]]
* Easy monitoring through AWS CloudWatch
* Easy to **get more resources per functions** (up to 10GB of RAM!) -> Also Improve **CPU & Network**

# Limits of Lambda
---

* Execution
	* **Memory allocation**: 128 MB – 10GB (1 MB increments)
	* **Maximum execution time**: 900 seconds (15 minutes)
	* **Environment variables** (4 KB)
	* **Disk capacity in the “function container” (in /tmp)**: 512 MB to 10GB
	* **Concurrency executions**: 1000 (can be increased)
* Deployment
	* Lambda function deployment size (compressed .zip): **50 MB**
	* Size of uncompressed deployment (code + dependencies): **250 MB**
	* Can use the **/tmp directory** to load other files at startup
	* Size of environment variables: **4 KB**

# Language Support
---

* Node.js (JavaScript) 
* Python
* Java (Java 8 compatible) 
* C# (.NET Core) 
* Golang 
* C# / Powershell 
* Ruby 
* Custom Runtime API (community supported, example Rust)
* Lambda Container Image 
	* The container image **must implement the Lambda Runtime API**
	* **ECS / Fargate** is preferred for running arbitrary Docker images

# Integrated Services
---

![[Pasted image 20230818081824.png]]

# Pricing
---

* Pay for Calls 
	* **First 1,000,000 requests are free**
	* **$0.20 per 1 million requests** thereafter ($0.0000002 per request)
* Pay for Durations
	* **400,000 GB -seconds of compute time per month for FREE**
		* **400,000 seconds if function is 1GB RAM** & **3,200,000 seconds if function is 128 MB RAM**
	* After that **$1.00 for 600,000 GB-seconds**

# Use Case / Example
---

# Serverless Thumbnail Creation
---

![[Pasted image 20230818082353.png]]

# CRON / Schedule Job
---

![[Pasted image 20230818082429.png]]

# Use With VPC to Connect to RDS
---

* [[04 Lambdas with VPC|Example]]