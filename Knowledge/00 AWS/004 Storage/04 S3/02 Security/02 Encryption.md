# Methods
---

## Server-Side Encryption
---

### Server-Side Encryption with **Amazon S3-Managed Keys** (SSE-S3)
---

* Header: "**x-amz-server-side-encryption: AES256**"
* Enabled **by default** for new buckets & new objects (But can be forced to **SSE-KMS** & **SSE-C**)

![[Pasted image 20230815131824.png]]

### Server-Side Encryption with **KMS Keys stored in AWS KMS** (SSE-KMS)
---

* Header: "**x-amz-server-side-encryption: aws:kms**"
* Pros & Cons
	* Advantage
		* **User Control** 
		* **Audit key usage** using CloudTrail
	* DisAdvantage
		* Calls **GenerateDataKey** KMS API & **Decrypt** KMS API, Impacted by **KMS Limits**

![[Pasted image 20230815132049.png]]


### Server-Side Encryption with **Customer-Provided Keys** (SSE-C)
---

* Using keys fully managed **by the customer outside of AWS** (Not store **the encryption provided**)
	* **HTTPS & Encryption Keys** should be provided

![[Pasted image 20230815132928.png]]

# Client-Side Encryption
---

* Use client libraries (E.g. **Amazon S3 Client-Side Encryption Library**)
* Clients fully **manages the key & encryption cycle**, must **encrypt & retrieve data themselves** before sending to Amazon S3

![[Pasted image 20230815133509.png]]
