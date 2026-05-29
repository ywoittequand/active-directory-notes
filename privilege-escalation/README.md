# Privilege Escalation

## Overview

Privilege escalation techniques are frequently leveraged during Active Directory assessments to move from low-privileged access toward administrative control.

## Common Scenarios

- Weak ACLs
- Misconfigured services
- Token abuse
- Credential exposure
- Delegation abuse

## Enterprise Risks

Privilege escalation may lead to:

- Domain compromise
- Sensitive data exposure
- Lateral movement opportunities
- Persistence mechanisms

## Methodology Focus

- Enumeration
- Privilege analysis
- Misconfiguration identification
- Attack path validation

## Common Tools

- BloodHound
- PowerView
- SharpHound
- Impacket
- Mimikatz
- Rubeus

## Defensive Considerations

- Least privilege enforcement
- Tiered administration
- Privileged account monitoring
- Service account hardening
- ACL reviews

## References

- MITRE ATT&CK
- SpecterOps Research
- Microsoft Security Baselines
