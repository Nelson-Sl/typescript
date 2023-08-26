# What's AWS Backup?
---

* Fully managed service that centrally **manage and automate backups across AWS services**
	* No need to **create custom scripts and manual processes**
	* Supports **cross-region** & **cross-account** backups

![[Pasted image 20230823195441.png]]

# Backup Features / Settings
---

* **Supports PITR for supported services** (Can recover to any point-in-time)
* **On-Demand** and **Scheduled** backups
* **Tag-based** backup policies


## Backup Plans
---

* **Backup frequency** (every 12 hours, daily, weekly, monthly, cron expression) 
* **Backup window** 
* Transition to **Cold Storage** (Never, Days, Weeks, Months, Years) 
* **Retention Period** (Always, Days, Weeks, Months, Years)

## Backup Vault Lock
---

* Enforce a **WORM (Write Once Read Many)** state for all the backups that you store in your AWS Backup Vault
* Additional layer of defense to protect your backups against:
	* **Inadvertent** or **malicious** delete operations
	* Updates that **shorten** or **alter** retention periods
* Even the **root user cannot delete backups when enabled**

![[Pasted image 20230823200541.png]]
