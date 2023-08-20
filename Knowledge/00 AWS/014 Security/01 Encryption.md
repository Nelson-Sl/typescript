# Encryption in flight (SSL)
---

* Data is **encrypted before sending** and **decrypted after receiving** through SSL Certificates
* Ensures no **MITM (man in the middle attack)** can happen

![[Pasted image 20230820164346.png]]

# Server side encryption at rest
---

* Data is **decrypted before being sent** & **encrypted after being received by the server**
* Stored in **an encrypted form like a key** (usually a data key)
* The encryption / decryption keys **must be managed somewhere** and **the server must have access to it**

![[Pasted image 20230820164753.png]]

# Client side encryption
---

* Data is **encrypted by the client** (never decrypted by the server) & will **be decrypted by a receiving client**
* Could **leverage Envelope Encryption**

![[Pasted image 20230820165017.png]]
