# Defensive Notes

## Overview

Defending against Kerberoasting requires a combination of strong password management, service account governance, and continuous monitoring.

Because ticket requests are often legitimate Kerberos operations, prevention is generally more effective than detection alone.

---

# Service Account Management

## Reduce Privileges

Apply the principle of least privilege.

Service accounts should possess only the permissions required for their function.

---

## Remove Legacy Accounts

Regularly identify and remove:

* Unused accounts
* Obsolete services
* Dormant administrative accounts

---

## Password Policies

Use:

* Long passwords
* Unique passwords
* Frequent rotation

---

## Group Managed Service Accounts (gMSA)

Deploy gMSA wherever possible.

Benefits include:

* Automatic password rotation
* Strong password generation
* Reduced administrative overhead

---

# Monitoring

Monitor for:

* Unusual Kerberos activity
* Service account abuse
* Privileged account activity
* Attack path exposure

---

# Assessment Reviews

Regularly review:

* Service account inventory
* Privilege assignments
* Tier 0 exposure
* BloodHound findings

---

# Strategic Defenses

Focus on:

1. Service account governance
2. Password hygiene
3. Privilege reduction
4. Tier 0 protection
5. Continuous attack path analysis

---

# References

* Microsoft Security Guidance
* MITRE ATT&CK
* SpecterOps Research
