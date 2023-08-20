# What's Multi-Region Key in KMS?
---

*  **Identical KMS keys in different AWS Regions** that can be used interchangeably
	* Have the **same key ID, key material, automatic rotation…**
	* **Encrypt in one Region and decrypt in other Regions** & No need to re-encrypt or making cross-Region API calls

# How does Multi-Region Key Works?
---

* Work with DynamoDB Global Tables Or Aurora Global D