# What's Multi-Region Key in KMS?
---

*  **Identical KMS keys in different AWS Regions** that can be used interchangeably
	* Have the **same key ID, key material, automatic rotation…**
	* **Encrypt in one Region and decrypt in other Regions** & No need to re-encrypt or making cross-Region API calls

![[Pasted image 20230820181236.png]]

## Notes
---

* KMS Multi-Region **are NOT global** (Primary + Replicas)
* Each Multi-Region key **is managed independently**

# How does Multi-Region Key Works?
---

* Work with **DynamoDB Global Tables** Or **Aurora Global Database**
* The client-side encrypted data is **replicated to other regions**, clients in these regions **can use low-latency API calls to KMS** in their region to decrypt the data client-side
* Using client-side encryption we can **protect specific fields** and **guarantee only decryption if the client has access to an API key**, we can protect specific fields **even from database admins**

![[Pasted image 20230820180913.png]]

# Use Case
---

* Global **client-side encryption**
* Encryption on **Global DynamoDB, Global Aurora**