# What's KMS?
---

* A fully managed service that **manages encryption keys for us**
	* Easy way to **control access to your data**
	* Seamlessly integrated into **most AWS services (EBS, S3, RDS, SSM…)**
	* Available through **API calls (SDK, CLI)** & Secrets **can be stored in the code / environment variables**

# Type of Keys
---

## Encryption Type
---

### Symmetric (AES-256 keys)
---

* **Single encryption key** that is used to Encrypt and Decrypt
* **Never get access to the KMS Key unencrypted** (must call KMS API to use)
* **Default Customer-Managed Keys** that used to integrate with KMS

### Asymmetric (RSA & ECC key pairs)
---

* **Public (Encrypt) and Private Key (Decrypt) pair** for Encrypt/Decrypt, or Sign/Verify operations
* The public key is downloadable, but **you can’t access the Private Key unencrypted**
* Use Case
	* **Encryption outside of AWS by users** who can’t call the KMS API

## KMS Key Type
---

* AWS Owned Keys (free)
	* **SSE-S3, SSE-SQS, SSE-DDB** (default key)
* AWS Managed Key: free (aws/service-name, example: aws/rds or aws/ebs)