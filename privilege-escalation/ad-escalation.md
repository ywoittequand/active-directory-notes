# Active Directory Privilege Escalation

## Overview

Active Directory privilege escalation focuses on abusing relationships, permissions, and configurations to obtain higher privileges within the domain.

---

## Common Escalation Sources

### ACL Abuse

Excessive permissions on users, groups, or computers.

### Group Membership Abuse

Mismanaged administrative groups.

### Delegation Abuse

Improper delegation configurations.

### Service Account Exposure

Compromised service accounts with elevated privileges.

---

## Assessment Methodology

1. Enumerate privilege relationships
2. Analyze BloodHound paths
3. Review delegated permissions
4. Validate attack paths

---

## Common Objectives

* Domain Admin
* Enterprise Admin
* Tier 0 Assets

---

## Enterprise Risks

* Domain compromise
* Forest compromise
* Long-term persistence
