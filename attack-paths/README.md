# Active Directory Attack Paths

## Overview

Attack paths represent the sequence of relationships, permissions, misconfigurations, and privilege escalation opportunities that an attacker may leverage to compromise an Active Directory environment.

Modern enterprise attacks rarely rely on a single vulnerability. Instead, attackers chain multiple weaknesses together in order to move laterally, escalate privileges, and ultimately compromise high-value assets.

Understanding attack paths is critical during internal penetration tests, assumed breach scenarios, and Red Team engagements.

---

## Key Concepts

### Privilege Relationships

Attack paths are often created through:

- Excessive permissions
- Nested group memberships
- Delegation misconfigurations
- Credential exposure
- Weak segmentation
- Local administrator reuse

### Attack Chaining

Attackers commonly combine:

1. Initial access
2. Enumeration
3. Privilege escalation
4. Credential abuse
5. Lateral movement
6. Persistence

---

## Common Objectives

- Identify privilege escalation opportunities
- Discover hidden administrative paths
- Evaluate lateral movement possibilities
- Assess enterprise exposure
- Validate attack chains toward Tier 0 assets

---

## Common Tools

- BloodHound
- SharpHound
- PowerView
- Impacket
- CrackMapExec

---

## Common Enterprise Risks

- Domain compromise
- Credential theft
- Excessive privilege exposure
- Weak AD tiering
- Insecure delegation

---

## Defensive Considerations

- Least privilege enforcement
- Tiered administration
- Session isolation
- ACL reviews
- Administrative segmentation
- Continuous attack path analysis

---

## References

- SpecterOps Research
- MITRE ATT&CK
- Microsoft Security Guidance
