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
* De