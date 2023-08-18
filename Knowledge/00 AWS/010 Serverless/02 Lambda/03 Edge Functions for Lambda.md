# What's Edge Function?
---

* A code that you **write and attach to CloudFront distributions** so that **you can run close to your users to minimize latency**
* You **don’t have to manage any servers**, deployed globally (Fully Serverless)
* Pay only for what you use

## Use Case
---

* **Customize the CDN content**

# How Edge Function Used in AWS?
---

## CloudFront Functions
---

* **Native feature of Cloudfront** (manage code entirely within CloudFront)
* **Lightweight functions** written in JavaScript that used to change **Viewer requests and responses** (After Cloudfront receive request & Before Cloudfront send response to viewer)

![[Pasted image 20230818085347.png]]

## Lambda@Edge
----

* **Lambda functions** written in NodeJS or Python that used to **change CloudFront requests and responses from Viewer & Origin side**

![[Pasted image 20230818093338.png]]

# CloudFront Functions vs Lambda@Edge
---

![[Pasted image 20230818102559.png]]

## CloudFront Functions
---

* Faster Execution Time & Number of Request Processing, good for For **high-scale, latency-sensitive CDN customizations**
	* Cache key normalization - Transform **request attributes (headers, cookies, query strings, URL)** to create an optimal Cache Key
	* Header manipulation - **Insert/modify/delete HTTP headers in the request or response**
	* **URL rewrites or redirects**
	* **Request authentication & authorization** - Create and validate user-generated tokens (e.g., JWT) to allow/deny requests

## Lambda@Edge
---

* Adjustable CPU or memory, Provide **Network access** to use external services for processing, **File system access** or **access to the body of HTTP requests**
* Good for less latency-sensitive & Complicated Work 
	* E.g. **A/B Testing**, Dynamic Web Application at the Edge, etc.

# Use Case
---

* Website Security and Privacy 
* Dynamic Web Application at the Edge 
* Search Engine Optimization (SEO) 
* Intelligently Route Across Origins and Data Centers 
* Bot Mitigation at the Edge • Real-time Image Transformation • A/B Testing • User Authentication and Authorization • User Prioritization • User Tracking and Analytics