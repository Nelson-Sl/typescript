# S3
---

* Need to enable the option that **enable objects encrypted with SSE-KMS**
	* **Specify which KMS Key to encrypt the objects** within the target bucket
	* Adapt the KMS Key Policy for the target key
		* An IAM Role with **kms:Decrypt for the source KMS Key** and **kms:Encrypt for the target KMS Key**
• You might get KMS throttling errors, in which case **you can ask for a Service Quotas increase**

## Multi-Region Keys
---

* Can use multi-region AWS KMS Keys, but they are currently treated as independent keys by Amazon S3 (the object will still be decrypted and then encrypted)
