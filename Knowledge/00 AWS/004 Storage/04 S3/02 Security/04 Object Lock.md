
* S3 Provide Object Lock to protect **data compliance & retention**, which adopts **WORM** model (Write Once, Read Many)

# Glacier Vault Lock
---

* Create a Vault Lock Policy to **lock for future edits** (can no longer be changed or deleted)

# S3 Object Lock
---

* Block an object version deletion for a specified amount of time (Decided by **Retention Period**)
	* Prerequisite: **Versioning must be enabled**
	* Retention Mode:
		* **Compliance**: Object versions **can't be overwritten or deleted by any user, including the root user**, nor it can change the **retention mode & period**
		* **Governance**: Most users can't overwrite or delete an object version or alter its lock settings, **some user has special permissions**
		* **Legal Hold**: protect the object **indefinitely**, independent from retention period (moved by appling **s3:PutObjectLegalHold** permission)