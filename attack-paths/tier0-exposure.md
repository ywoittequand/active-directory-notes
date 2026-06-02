# Tier 0 Exposure

## Overview

Tier 0 represents the most critical assets within an Active Directory environment.

Compromise of a Tier 0 asset may result in full control of the identity infrastructure and ultimately lead to complete domain compromise.

Modern Active Directory assessments should focus not only on vulnerabilities but also on identifying attack paths leading to Tier 0 assets.

---

## What is Tier 0?

Tier 0 includes systems, accounts, and services that directly control identity, authentication, authorization, and security boundaries.

Examples include:

- Domain Controllers
- Enterprise Admins
- Domain Admins
- PKI Infrastructure (ADCS)
- Azure AD Connect
- Active Directory Federation Services (ADFS)
- Privileged Access Workstations (PAW)
- Identity Management Platforms

---

## Why Tier 0 Matters

Attackers rarely need to compromise every system.

Instead, they seek paths toward Tier 0 assets because control of these assets often provides:

- Domain dominance
- Persistence
- Credential access
- Administrative control
- Long-term access

---

## Common Tier 0 Exposure Scenarios

### Excessive Administrative Privileges

Administrative privileges granted beyond operational requirements.

Potential Impact:

- Privilege escalation
- Attack path expansion
- Increased attack surface

---

### Service Account Exposure

Privileged service accounts with weak passwords or excessive permissions.

Potential Impact:

- Kerberoasting opportunities
- Lateral movement
- Domain compromise

---

### Uncontrolled Delegation

Delegation configurations exposing privileged accounts.

Potential Impact:

- Credential theft
- Authentication abuse
- Privilege escalation

---

### Session Exposure

Tier 0 administrators logging into lower-trust systems.

Potential Impact:

- Credential dumping
- Token theft
- Administrative account compromise

---

### ADCS Misconfigurations

Weak certificate templates or enrollment permissions.

Potential Impact:

- Certificate abuse
- Persistence
- Domain escalation

---

## Attack Path Examples

### Example 1

Low Privileged User

↓

Kerberoastable Service Account

↓

Server Administrator

↓

Domain Controller Access

↓

Domain Admin

---

### Example 2

Compromised Workstation

↓

Privileged Session Exposure

↓

Credential Extraction

↓

Administrative Access

↓

Tier 0 Compromise

---

### Example 3

Delegated Permissions

↓

ACL Abuse

↓

Group Membership Modification

↓

Administrative Rights

↓

Tier 0 Access

---

## Assessment Methodology

### Step 1 – Identify Tier 0 Assets

Inventory:

- Domain Controllers
- Administrative Groups
- PKI Systems
- Identity Infrastructure

---

### Step 2 – Map Privilege Relationships

Analyze:

- ACLs
- Group memberships
- Delegation
- Administrative boundaries

---

### Step 3 – Identify Attack Paths

Review:

- BloodHound shortest paths
- Session exposure
- Local administrator relationships
- Service account privileges

---

### Step 4 – Validate Exposure

Determine:

- Feasibility
- Business impact
- Required attacker privileges

---

## BloodHound Analysis Focus

When reviewing BloodHound data, prioritize:

### High Value Targets

- Domain Admins
- Enterprise Admins
- Domain Controllers
- Certificate Authorities

### Common Dangerous Edges

- GenericAll
- GenericWrite
- WriteDACL
- WriteOwner
- AddMember
- ForceChangePassword

### Common Indicators

- Large attack path counts
- Excessive privilege inheritance
- Tier 0 reachable from standard users

---

## Enterprise Risks

Tier 0 exposure may result in:

- Full Active Directory compromise
- Long-term persistence
- Trust relationship compromise
- Credential theft
- Security control bypass

---

## Defensive Considerations

### Administrative Tiering

Separate administrative activities from standard user operations.

### Privileged Access Workstations

Restrict privileged administration to dedicated systems.

### Least Privilege

Review delegated permissions regularly.

### Session Isolation

Prevent Tier 0 accounts from logging onto lower-trust systems.

### Continuous Attack Path Analysis

Regularly review privilege relationships using tools such as BloodHound.

### ADCS Hardening

Review certificate templates and enrollment permissions.

---

## Common Tools

- BloodHound
- SharpHound
- PowerView
- PingCastle
- Purple Knight

---

## References

- SpecterOps Research
- Microsoft Tiering Model
- Microsoft Enterprise Access Model
- BloodHound Documentation
- MITRE ATT&CK
