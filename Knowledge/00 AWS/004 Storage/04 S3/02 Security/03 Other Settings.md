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

