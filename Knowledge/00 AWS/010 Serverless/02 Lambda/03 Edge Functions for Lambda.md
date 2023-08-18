# What's Edge Functions?
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

* Faster Execution Time & Number of Request Processing, good for **short & quick work change**
	* Cache key normalization - Transform **request attributes (headers, cookies, query strings, URL)** to create an optimal Cache Key
	* 