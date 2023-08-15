# Baseline
---

* automatically **scales to high request rates**, latency **100-200** ms
* can achieve at least **3,500 PUT/COPY/POST/DELETE** or **5,500 GET/HEAD** requests per second per prefix in a bucket.

# Improve Performance
---

## Multi-Part Upload
---

* Must for files **> 5GB** and Suggests for **> 100 Mb**
* Can help for **parallel transfer**

![[Pasted image 20230815022227.png]]

## S3 Transfer Acceleration
---

* Increase transfer speed by **transferring file to an AWS edge location** which will forward the data to the S3 bucket in the target region (Compatible with multi-part upload)

![[Pasted image 20230815022331.png]]

## Byte-Range Fetches
---

* Parallelize GETs by **requesting specific byte ranges** (Better resilience in case of failures)
	* Can **speed up downloads** (Request in Parallel) & **Retrieve only partial data**

![[Pasted image 20230815022626.png]]
