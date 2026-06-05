# SPN Enumeration

## Overview

Service Principal Names (SPNs) are identifiers used by Kerberos to associate services with service accounts.

SPN enumeration is the first step in a Kerberoasting assessment.

The objective is to identify service accounts that may be targeted for offline password attacks.

---

## What Is an SPN?

An SPN uniquely identifies a service instance within an Active Directory environment.

Examples include:

* MSSQLSvc
* HTTP
* CIFS
* LDAP
* HOST

---

## Why SPNs Matter

Any authenticated domain user can typically request Kerberos service tickets for SPN-enabled accounts.

These tickets may become candidates for offline password cracking.

---

## Assessment Goals

Identify:

* Service accounts
* Privileged service accounts
* Legacy service accounts
* High-value targets

---

## High-Risk Indicators

### Privileged Accounts

Service accounts that belong to:

* Domain Admins
* Server Administrators
* Backup Operators

---

### Legacy Accounts

Accounts that:

* Have not changed passwords recently
* Use static passwords
* Have excessive permissions

---

### Critical Infrastructure Accounts

Accounts supporting:

* SQL Servers
* SCCM
* Backup Platforms
* Monitoring Systems

---

## Risk Evaluation

During assessments evaluate:

* Account privileges
* Password management practices
* Business criticality
* Exposure to attack paths

---

## References

* Microsoft Kerberos Documentation
* SpecterOps Research
