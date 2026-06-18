# Defensive Notes

## Overview

Mitigating NTLM Relay requires reducing reliance on NTLM and strengthening authentication protections across the environment.

---

# Defensive Priorities

## SMB Signing

Enforce SMB signing wherever possible.

---

## LDAP Signing

Require LDAP signing and channel binding.

---

## Reduce NTLM Usage

Limit legacy authentication dependencies.

---

## Harden ADCS

Review:

* Certificate templates
* Enrollment permissions
* Web enrollment exposure

---

## Administrative Segmentation

Protect Tier 0 systems from lower-trust networks.

---

## Monitoring

Monitor for:

* Unusual NTLM activity
* Authentication anomalies
* Relay-related behavior

---

# References

* Microsoft Security Guidance
* SpecterOps Research
* MITRE ATT&CK
