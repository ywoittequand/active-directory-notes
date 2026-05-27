# Kerberoasting

## Overview

Kerberoasting is an Active Directory attack technique allowing authenticated users to request Kerberos service tickets (TGS) associated with Service Principal Names (SPNs), which can then be cracked offline to recover service account passwords.

## Why It Matters

Weak service account passwords remain common in enterprise environments and may lead to:

- Privilege escalation
- Lateral movement
- Domain compromise

## Typical Attack Workflow

1. Enumerate SPNs
2. Request TGS tickets
3. Extract Kerberos hashes
4. Perform offline password cracking
5. Reuse compromised credentials

## Common Tools

- Impacket
- Rubeus
- Hashcat

## Detection Considerations

Potential indicators include:

- Unusual volume of TGS requests
- Service ticket enumeration activity
- Kerberos anomalies

## Mitigation Recommendations

- Strong service account passwords
- Group Managed Service Accounts (gMSA)
- Least privilege principles
- Kerberos monitoring

## References

- MITRE ATT&CK T1558.003
- SpecterOps
- Microsoft Security Guidance
