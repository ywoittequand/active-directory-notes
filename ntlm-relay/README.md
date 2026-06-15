# NTLM Relay

## Overview

NTLM Relay is an attack technique that abuses NTLM authentication to relay authentication requests toward other services.

The attack allows an attacker to authenticate as another user without directly knowing their password.

NTLM Relay remains highly relevant in modern Active Directory environments due to legacy authentication protocols and misconfigurations.

---

# Objectives

* Gain authenticated access
* Escalate privileges
* Abuse trust relationships
* Expand attack paths

---

# Common Targets

* SMB
* LDAP
* HTTP
* ADCS
* MSSQL

---

# Enterprise Risks

* Privilege escalation
* Administrative compromise
* Certificate abuse
* Domain compromise

---

# References

* SpecterOps Research
* Microsoft Security Guidance
* MITRE ATT&CK
