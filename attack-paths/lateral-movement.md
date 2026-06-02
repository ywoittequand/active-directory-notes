# Lateral Movement Attack Paths

## Overview

Lateral movement is a critical component of Active Directory attack paths.

After obtaining an initial foothold, attackers attempt to move across systems, identify privileged accounts, and reach high-value assets such as application servers, management systems, and Domain Controllers.

Successful lateral movement often relies on misconfigurations, credential exposure, weak segmentation, and excessive administrative privileges.

---

# Common Lateral Movement Attack Paths

## Path 1 – Local Administrator Reuse

### Scenario

The same local administrator password is deployed across multiple workstations or servers.

### Attack Flow

1. Compromise Workstation A
2. Extract local administrator credentials
3. Authenticate to Workstation B
4. Dump additional credentials
5. Continue expansion across the environment

### Enterprise Risk

A single compromised endpoint may lead to widespread access across the network.

---

## Path 2 – Administrative Session Exposure

### Scenario

A privileged administrator logs into a compromised workstation.

### Attack Flow

1. Compromise user workstation
2. Identify active administrative sessions
3. Extract privileged credentials or tokens
4. Access management systems
5. Escalate privileges

### Enterprise Risk

Exposure of highly privileged accounts through insecure administration practices.

---

## Path 3 – Service Account Compromise

### Scenario

A service account is compromised through Kerberoasting or password exposure.

### Attack Flow

1. Enumerate service accounts
2. Obtain service account credentials
3. Access systems managed by the account
4. Discover additional privileges
5. Escalate toward administrative access

### Enterprise Risk

Excessive service account privileges may create direct attack paths to Tier 0 assets.

---

## Path 4 – SMB Administrative Access

### Scenario

Compromised credentials provide local administrator access on multiple systems.

### Attack Flow

1. Identify accessible systems
2. Access administrative shares
3. Execute commands remotely
4. Enumerate credentials
5. Continue lateral movement

### Enterprise Risk

Weak privilege boundaries facilitate attacker movement.

---

## Path 5 – WinRM-Based Lateral Movement

### Scenario

Remote management services are broadly accessible.

### Attack Flow

1. Compromise privileged credentials
2. Identify WinRM-enabled systems
3. Execute remote PowerShell sessions
4. Perform reconnaissance
5. Expand access

### Enterprise Risk

Poor access control around remote administration services.

---

## Path 6 – BloodHound-Derived Attack Paths

### Scenario

Privilege relationships create indirect routes to privileged assets.

### Attack Flow

1. Collect BloodHound data
2. Identify shortest paths to Domain Admin
3. Analyze ACL relationships
4. Abuse delegated permissions
5. Reach high-value targets

### Enterprise Risk

Hidden privilege relationships expose critical systems.

---

# Common Root Causes

Lateral movement paths are frequently enabled by:

- Local administrator password reuse
- Weak segmentation
- Excessive privileges
- Credential exposure
- Poor administrative hygiene
- Uncontrolled delegation

---

# Assessment Methodology

## Step 1 – Enumerate Assets

Identify:

- Hosts
- Servers
- Domain Controllers
- Administrative systems

---

## Step 2 – Identify Credentials

Review:

- Active sessions
- Service accounts
- Stored credentials
- Administrative accounts

---

## Step 3 – Map Relationships

Analyze:

- Group memberships
- ACLs
- Local administrators
- Delegation settings

---

## Step 4 – Validate Attack Paths

Confirm:

- Access possibilities
- Privilege escalation opportunities
- Business impact

---

# High-Value Targets

Common objectives include:

- Domain Controllers
- PKI infrastructure
- Backup servers
- Virtualization platforms
- Identity management systems

---

# Defensive Considerations

## Network Segmentation

Reduce unnecessary host-to-host communication.

## Administrative Tiering

Separate administrative activities from user systems.

## Local Administrator Management

Implement Windows LAPS.

## Session Protection

Limit privileged logons on lower-trust systems.

## Continuous Attack Path Analysis

Regularly review BloodHound findings and privilege relationships.

---

# References

- SpecterOps Research
- BloodHound Documentation
- MITRE ATT&CK
- Microsoft Security Guidance
