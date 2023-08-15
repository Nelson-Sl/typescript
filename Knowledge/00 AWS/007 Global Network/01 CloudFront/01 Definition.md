# What's CloudFront ?
---

* It's a **Content Delivery Network (CDN)** service provided by AWS
	* **216 Point of Presence globally** (edge locations)

![[Pasted image 20230815201626.png]]

# How CloudFront Works:
---

* Files are **cached for a TTL** (maybe a day)

![[Pasted image 20230815202349.png]]

# When use CloudFront: Support Origins
---

* [[02 Origin S3 Bucket|S3 Bucket]]
* Custom HTTP Origins
	* [[03 Origin ALB & EC2|Application Load Balancer]]
	* [[03 Origin ALB & EC2|EC2 instance]]
	* S3 website (must first **enable the bucket as a static S3 website**)
	* Any HTTP backend you want
# CloudFront Security
---
* OutBound
	* **DDoS protection** (because worldwide) with integration to **Shield**
	* AWS **Web Application Firewall**
* InBound
	* **OAC** (Origin Access Control)

# Other Features
---

* [[04 Geo Restriction|Geo Restriction]]
* [[05 Cache Invalidation|Cache Invalidation]]

# Price
---

## Per Month Price
---

![[Pasted image 20230815204608.png]]

## Price Classes
---

1. Price Class All: **all regions** – best performance
2. Price Class 200: most regions, **but excludes the most expensive regions**
3. Price Class 100: **only the least expensive regions**

![[Pasted image 20230815204902.png]]

![[Pasted image 20230815204932.png]]

# Why use Cloudfront
---

* Global Edge Network, great for **static content that must be available everywhere**
* Improve User Experience