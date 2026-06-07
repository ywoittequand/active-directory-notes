# Service Account Abuse

## Overview

Service accounts frequently possess elevated privileges and represent attractive targets during Active Directory assessments.

---

## Common Risks

### Excessive Permissions

Service accounts granted administrative privileges.

### Legacy Passwords

Static passwords used for years.

### Critical Infrastructure Access

Accounts managing:

* SQL Servers
* SCCM
* Backup Platforms
* Monitoring Systems

---

## Assessment Methodology

1. Identify service accounts
2. Review privileges
3. Assess attack paths
4. Evaluate Tier 0 exposure

---

## Potential Impact

* Privilege escalation
* Lateral movement
* Persistence
* Domain compromise

---

## Defensive Recommendations

* gMSA adoption
* Password rotation
* Least privilege
* Service account reviews
