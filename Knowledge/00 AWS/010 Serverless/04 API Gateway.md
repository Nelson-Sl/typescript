# What's API Gateway?
---


* **Create, Maintain & Secure APIs** at any scale
	* Transform and validate requests and responses
	* Support **HTTP, Websocket, REST (Public & Private)** Protocol
	* Handle **API versioning** (v1, v2…), **different environments** (dev, test, prod…) & **security** (Authentication and Authorization)

# Features
---

* Security & Throttling
	* Create **API keys**, handle **request throttling**
* **Documentation**
	* **Swagger / Open API** import to quickly define APIs
	* Generate SDK and API **specifications**
* **Cache API responses**

# Endpoint Types
---

* Edge-Optimized (default)
	* The API Gateway **still lives in only one region** but **requests are routed through the CloudFront Edge locations** (improves latency)
	* For global clients
* Regional
	* For clients **within the same region**
	* Could **manually combine with CloudFront** (more control over the caching strategies and the distribution)
* Private
	* Can **only be accessed from your VPC** using an interface VPC endpoint (ENI)
	* Use a **resource policy** to define access

# Integration & Use Cases
---

## Lambda Function
---

* Invoke Lambda Function ( API Gateway + Lambda **has no infrastructure to manage**)
* Easy way to expose REST API backed by AWS Lambda

![[Pasted image 20230818153155.png]]

## HTTP
---

* Expose HTTP endpoints in the backend (**Internal HTTP API on premise**, ALB...)
	* Can add **rate limiting**, **caching**, **user authentications**, **API keys**, etc…

## Other AWS Service
---

* **Expose any AWS API through the API Gateway** (E.g. start an AWS Step Function workflow, Post a message to SQS)
	* Can add **authentication**, **deploy publicly**, **rate control**

## Example: Integrate with Kinesis Data Stream
---

![[Pasted image 20230818153739.png]]

# Security
---

* Authentication
	* IAM Roles (useful for **internal applications**)
	* Cognito (identity for **external users** – example mobile users)
	* Custom Authorizer (your own logic)
* Custom HTTPS Domain Name -> Provide Security through 