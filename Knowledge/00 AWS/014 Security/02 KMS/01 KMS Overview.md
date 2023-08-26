# What's KMS?
---

* A fully managed service that **manages encryption keys for us**
	* Easy way to **control access to your data**
	* Seamlessly integrated into **most AWS services (EBS, S3, RDS, SSM…)**
	* Available through **API calls (SDK, CLI)** & Secrets **can be stored in the code / environment variables**

## Integration With Other Service
---

* Fully **integrated with IAM for authorization**
* Able to **audit KMS Key usage using CloudTrail**

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
* AWS Managed Key
	* free (**aws/service-name**, example: aws/rds or aws/ebs)
	* **Automatically rotated in 1 year**
* Customer managed keys (CMK)
	* Created in KMS: **$1 / month**, **Automatically rotated in 1 year** (must be enabled)
	* Imported (must be symmetric key): **$1 / month + pay for API call to KMS ($0.03 / 10000 calls)**, only **manual rotation** possible using alias

# Key Policies
---

* Control **access to KMS keys**
* Default Key Policy
	* Created if you **don’t provide a specific KMS Key Policy**
	* **Complete access to the key to the root user** = entire AWS account
* Custom Key Policy
	* Define **users, roles that can access the KMS key**
	* Define who **can administer the key**
	* **Useful for cross-account access** of your KMS key

# Backup: Copy Snapshot Between Regions
---

1. **Create a Snapshot, encrypted with your own KMS Key** (Customer Managed Key)
2. **Attach a KMS Key Policy to authorize cross-account access**
3. Share the encrypted snapshot
4. (in target) Create a copy of the Snapshot, encrypt it with a CMK in your account
5. Create a volume from the snapshot

![[Pasted image 20230820174157.png]]

# Other Feature
---

* [[02 Multi-Region Key|Multi-Region Key]]



