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

* S3 Bucket
* Custom HTTP Origins
	* Application Load Balancer (ALB)
	* EC2 instance
	* S3 website (must first **enable the bucket as a static S3 website**)
	* Any HTTP backend you want

# CloudFront Security
---
* OutBound
	* **DDoS protection** (because worldwide)
	* integration with **Shield**
	* AWS **Web Application Firewall**
* InBound
	* **OAC** (Origin Access Control)

# Why use Cloudfront
---

* DDoS protection (because worldwide), integration with Shield,
AWS Web Application Firewall