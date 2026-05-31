# Common Active Directory Attack Paths

## Overview

Attack paths in Active Directory environments are frequently created through combinations of weak permissions, credential exposure, and insufficient segmentation.

---

# Common Attack Path Examples

## 1. Local Administrator Reuse

### Scenario

A workstation local administrator password is reused across multiple systems.

### Potential Impact

- Lateral movement
- Credential dumping
- Expanded compromise scope

### Typical Attack Flow

1. Initial workstation compromise
2. Credential extraction
3. SMB or WinRM access
4. Pivot to additional systems

---

## 2. Kerberoasting to Privilege Escalation

### Scenario

Weak service account passwords associated with SPNs.

### Potential Impact

- Service account compromise
- Elevated privileges
- Domain escalation

### Typical Attack Flow

1. Enumerate SPNs
2. Request Kerberos tickets
3. Offline password cracking
4. Reuse compromised credentials

---

## 3. NTLM Relay Attack Paths

### Scenario

SMB signing disabled combined with authentication coercion.

### Potential Impact

- Unauthorized access
- LDAP privilege abuse
- ADCS exploitation

### Typical Attack Flow

1. Coerce authentication
2. Relay NTLM authentication
3. Abuse relayed privileges
4. Escalate access

---

## 4. ACL Abuse

### Scenario

Excessive delegated permissions in Active Directory.

### Potential Impact

- Privilege escalation
- Persistence
- Hidden administrative access

### Typical Attack Flow

1. Enumerate ACLs
2. Identify delegated permissions
3. Abuse object control
4. Escalate privileges
