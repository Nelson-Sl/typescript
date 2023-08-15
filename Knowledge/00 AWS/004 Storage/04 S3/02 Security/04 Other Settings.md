# CORS
---

* Web Browser based mechanism to **allow requests to other origins** while visiting the main origin
	* Same origin: http://example.com/app1 & http://example.com/app2 (Domain, Host & Port should be the same)
	* Different origins: http://www.example.com & http://other.example.com
	* Controlled by **Access-Control-Allow-Origin** Headers
* In S3, to avoid CORS problems, we should **enable the correct CORS headers**

![[Pasted image 20230815165212.png]]

# MFA Delete
---

* It could be set as MFA required to **pernamently delete an object version** & **suspending versioning on the bucket** (Not required if list deleted version or enable versioning)
	* Prerequisite: Bucket Owner (Root Account) **should enable MFA delete**, Versioning should be **enabled**
## What's MFA?
---

**MFA (Multi-Factor Authentication)** –> force users to **generate a code on a device** (usually a mobile phone or hardware) before doing important operations on S3

# Pre-Signed URL
---

* Users given a pre-signed URL inherit the permissions of the user that **generated the URL for GET / PUT** (Usually a **temporary access**)
	* Can be generated from **S3 Console, AWS CLI or SDK**
	* Expiration Time
		* S3 Console: **1 min - 12 hours**
		* AWS CLI (Configured with **--expires-in**): Default **3600 sec**, maximum **604800 sec**

## Use Case
---

* Temporary Access: Allow t**emporarily** a user to upload a file to a precise location in your S3 bucket
* Restrict Access: Allow **only logged-in users** to download a premium video from your S3 bucket

# Access Points
---

Access Points **simplify security management for S3 Buckets**, which consists of:
* its own **DNS name** (Internet Origin or VPC Origin -> **VPC Endpoint to access the Access Point**)
* an **access point policy** (similar to bucket policy) – manage security at scale