# Kerberoasting

## Overview

Kerberoasting is an Active Directory attack technique that targets service accounts associated with Service Principal Names (SPNs).

The technique allows authenticated domain users to request Kerberos service tickets and perform offline password cracking attacks against service account credentials.

Kerberoasting remains one of the most common privilege escalation techniques identified during internal penetration tests and Active Directory security assessments.

---

## Objectives

The primary objective of Kerberoasting is to obtain service account credentials that may provide elevated privileges within the environment.

Successful compromise of service accounts can lead to:

* Privilege escalation
* Lateral movement
* Access to critical infrastructure
* Domain compromise

---

## Why Kerberoasting Matters

Many organizations assign excessive privileges to service accounts while using weak or outdated password management practices.

Service accounts frequently possess:

* Local administrator rights
* Administrative access to servers
* Access to databases
* Access to backup systems
* Domain-level privileges

---

## Kerberoasting Attack Chain

1. Identify SPNs
2. Request Kerberos service tickets
3. Extract ticket material
4. Perform offline password cracking
5. Validate credentials
6. Assess privileges
7. Expand access

---

## Common Targets

* SQL Service Accounts
* IIS Service Accounts
* SCCM Service Accounts
* Backup Service Accounts
* Monitoring Service Accounts

---

## Enterprise Risks

* Credential exposure
* Privilege escalation
* Lateral movement
* Domain compromise

---

## Defensive Considerations

* Strong passwords
* gMSA deployment
* Service account reviews
* Privilege reduction
* Kerberos monitoring

---

## References

* SpecterOps Research
* Microsoft Security Guidance
* MITRE ATT&CK
