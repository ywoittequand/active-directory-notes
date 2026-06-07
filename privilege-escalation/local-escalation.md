# Local Privilege Escalation

## Overview

Local privilege escalation allows attackers to increase privileges on a compromised host.

This often serves as a stepping stone toward lateral movement and domain compromise.

---

## Common Misconfigurations

### Weak Service Permissions

Services may allow unauthorized modification.

### Scheduled Task Misconfigurations

Improper permissions on scheduled tasks.

### Insecure Software Installations

Applications running with elevated privileges.

### Credential Exposure

Stored credentials or sensitive files.

---

## Assessment Methodology

1. Identify privilege level
2. Review installed software
3. Analyze services
4. Review scheduled tasks
5. Evaluate local groups

---

## Potential Impact

* Administrative access
* Credential extraction
* Lateral movement opportunities

---

## Defensive Considerations

* Least privilege
* Patch management
* Service hardening
* Credential protection
