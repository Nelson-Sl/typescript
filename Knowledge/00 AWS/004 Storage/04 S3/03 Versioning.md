# Definition
---

* S3 Supports **versioning** for s3 objects and it's **enabled at bucket level**
	* Easy to **roll back to previous version**
	* Protect against **unintended deletes** (ability to **restore a version**)

# Note
---

* Any file that is not versioned prior to enabling versioning will have version “**null**”
* Suspending versioning **does not delete the previous versions**