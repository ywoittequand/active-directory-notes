# Lateral Movement

## Overview

Lateral movement refers to techniques used by attackers to move from one compromised system to another within an environment.

In Active Directory environments, lateral movement often represents the transition between initial access and privileged compromise.

Understanding lateral movement is essential during internal penetration tests, assumed breach scenarios, and Active Directory assessments.

---

# Objectives

The goal of lateral movement is to:

* Expand access
* Reach critical systems
* Access privileged accounts
* Escalate privileges
* Reach Tier 0 assets

---

# Common Lateral Movement Sources

* Credential reuse
* Administrative privileges
* Session exposure
* Remote administration protocols
* Delegation abuse

---

# Enterprise Risks

Successful lateral movement may lead to:

* Domain compromise
* Credential theft
* Privilege escalation
* Persistence
* Data exposure

---

# Common Protocols

* SMB
* RDP
* WinRM
* WMI
* RPC

---

# Assessment Focus

During assessments, evaluate:

* Local administrator relationships
* Session exposure
* Administrative segmentation
* Credential management
* Tier 0 exposure

---

# References

* MITRE ATT&CK
* SpecterOps Research
* Microsoft Security Guidance
