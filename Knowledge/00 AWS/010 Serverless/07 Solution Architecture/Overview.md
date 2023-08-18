# To do list Example
---

* Authorization & Authentication
	* Cognito: **generate temporary credentials with STS to access S3 bucket with restricted policy**. App users can directly access AWS resources this way.
* Caching
	* Caching **the reads on DynamoDB using DAX**
	* Caching **the REST requests at the API Gateway level**

![[Pasted image 20230818164559.png]]

# Blog Example
---

* Serving Globally
	* **Distributed using CloudFront** with S3
	* Leveraged a **Global DynamoDB table** to serve the data globally
* Send Email
	* Enabled **DynamoDB streams** to trigger a Lambda function. In the end **SES (Simple Email Service)** was used to send emails in a serverless way

![[Pasted image 20230818165443.png]]

![[Pasted image 20230818165503.png]]

# MicroService Example
---

* Benefit Using Serverless Architecture
	* API Gateway, Lambda **scale automatically and you pay per usage** (Increase server utilization)
	* You can easily **clone API, reproduce environments** (Avoid repeated overhead for creating each new microservice)
	* **Generated client SDK through Swagger integration for the API Gateway** (Solve proliferation of client-side code requirements to integrate with many separate services)

![[Pasted image 20230818170136.png]]

# Software Update Example
---

* Cloudfront will cache software update files at the edge (and its static) and scale automatically
* we’ll save tremendously in EC2, as well as availability, network bandwidth cost
* No changes to architecture

![[Pasted image 20230818170837.png]]
