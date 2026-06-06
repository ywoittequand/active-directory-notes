# Password Cracking Considerations

## Overview

The success of Kerberoasting depends largely on the strength of service account passwords.

Offline analysis allows attackers to test password strength without interacting further with the target environment.

---

## Why Service Accounts Are Vulnerable

Organizations often:

* Reuse passwords
* Use predictable naming conventions
* Avoid password rotations
* Maintain legacy service accounts

---

## Common Weaknesses

### Human-Created Passwords

Examples:

* CompanyName2024
* Welcome123
* Summer2025

---

### Password Reuse

The same password used across:

* Multiple service accounts
* Administrative accounts
* Legacy systems

---

### Long-Lived Passwords

Passwords unchanged for years.

---

## Risk Factors

### High Privileges

Weak passwords combined with elevated privileges create significant risk.

### Critical Infrastructure

Compromise of service accounts supporting key systems increases impact.

---

## Assessment Focus

Evaluate:

* Password management practices
* Service account lifecycle
* Privilege assignments
* Exposure to attack paths

---

## Defensive Recommendations

* Deploy gMSA
* Enforce password rotation
* Review privileges regularly
* Remove obsolete accounts

---

## References

* Microsoft Security Guidance
* SpecterOps Research
