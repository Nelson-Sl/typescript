# Default: Automated Backup
---

Retention Days should be **1-35 days** & **Can't be Disabled**

# Manual DB Snapshot
---

Should be **triggered by user** & can keep the backup **as long as you want**

# Restoring Aurora From S3
---

* Steps: Create a backup of existing database using **Percona XtraBackup** -> Store the backup file in S3 -> **Restore the backup file** onto a new Aurora cluster

# Aurora Database Cloning
---

* Definition: Copy an existing Aurora database **to a new cluster** (usually they will **share the same data volume** and allocated new data storage when needed)
* Benefit: **Faster** than Restore & Snapshot, **Cost-Effective**
* Use Case: **Create a staging database** without impacting production

![[Pasted image 20230808002254.png]]