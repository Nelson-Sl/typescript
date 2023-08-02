# Password Policy
---

* Reason: Stronger the passwords, the **higher security**
* Available settings for password in Root Account:
	* Set up a **minimum password length**
	* Set up **required specific character types** (E.g. mixture of lowercase & uppercase letters, numbers, non-alphanumeric characters like _ )
	* Allow all IAM users to **change their own passwords** and require them to **change it after an expiration period**
	* Prevent **password re-use** when changing password

# Multi-Factor Authentication (MFA)
---

## What is MFA?
---

MFA should be passed with **your known password**, as well as **security device we own**

## Why MFA?
---
It can **protect your resources and configs** even if your root account and **IAM account was hacked or stolen**.

## What devices is supporting MFA?
---

* Virtual MFA Device
	* **Google Authenticator** (Mobile Phone)
	* **Authy** (Phone, Laptop & Tablet, Can **store multiple tokens** for different root & IAM users)
* Universal 2nd Factor (U2F) Security Key
	* **YubiKey** (Can **store multiple tokens** for different root & IAM users in a single key)
* Hardware Key Fob MFA Device
	* **Gemalto**
* Hardware Key Fob MFA Device For AWS GovCloud
	* **SurePassId**