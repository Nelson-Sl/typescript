# Automated Backup
---

* Will backup the database **once a day** and **transaction logs** every 5 minutes, can be **restored to any point of time**
* Have retention days of **1-35 days**, **can be disbled** by setting it to 0
# Manual DB Snapshot
---

Should be **triggered by user** & can keep the backup **as long as you want**

# Restoring Aurora From S3
---

* Steps: Create a backup of existing database -> Store the backup file in S3 -> **Restore the backup file** onto a new RDS instance
* Use case: Can **restore & Snapshot database** if wanna stop database for a long time since stopped RDS instance still pays for storage