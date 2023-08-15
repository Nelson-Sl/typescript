# CORS
---

* Web Browser based mechanism to **allow requests to other origins** while visiting the main origin
	* Same origin: http://example.com/app1 & http://example.com/app2 (Domain, Host & Port should be the same)
	* Different origins: http://www.example.com & http://other.example.com
	* Controlled by **Access-Control-Allow-Origin** Headers
* In S3, to avoid CORS problems, we should **enable the correct CORS headers**

![[Pasted image 20230815165212.png]]
