# High Value Targets

## Overview

High Value Targets (HVTs) are systems, accounts, and services that provide significant control over an organization's identity infrastructure, administrative functions, or critical business operations.

During Active Directory assessments, identifying and protecting these assets is a primary objective for defenders and a key focus for attackers.

BloodHound enables security professionals to visualize and prioritize attack paths leading to these critical assets.

---

# Why High Value Targets Matter

Attackers rarely need to compromise every system within an environment.

Instead, they focus on obtaining access to assets that provide:

* Administrative control
* Credential access
* Privilege escalation opportunities
* Persistence mechanisms
* Access to sensitive business data

Compromise of a High Value Target often results in complete domain compromise.

---

# Common High Value Targets

## Domain Controllers

### Description

Domain Controllers are the most critical systems in an Active Directory environment.

They manage:

* Authentication
* Authorization
* Group Policy
* Replication
* Kerberos

### Potential Impact

Compromise of a Domain Controller typically results in:

* Domain dominance
* Credential theft
* Persistence
* Full Active Directory compromise

---

## Domain Admins

### Description

Members of the Domain Admins group possess extensive administrative privileges across the domain.

### Potential Impact

* Administrative control
* Access to critical systems
* Privilege escalation opportunities

---

## Enterprise Admins

### Description

Enterprise Admins maintain administrative privileges across all domains within a forest.

### Potential Impact

* Forest-wide compromise
* Cross-domain access
* Complete identity infrastructure control

---

## Certificate Authorities (ADCS)

### Description

Active Directory Certificate Services manage certificate issuance and trust relationships.

### Potential Impact

* Certificate abuse
* Authentication bypass
* Long-term persistence
* Domain escalation

---

## Privileged Access Workstations (PAW)

### Description

Dedicated systems used for privileged administration.

### Potential Impact

Compromise may expose:

* Administrative credentials
* Sensitive management tools
* Tier 0 assets

---

## Identity Infrastructure

Examples include:

* Azure AD Connect
* Identity Management Platforms
* Federation Services

### Potential Impact

* Hybrid identity compromise
* Credential synchronization abuse
* Expanded attack paths

---

# High Value Accounts

## Domain Administrators

Administrative control over Active Directory.

---

## Enterprise Administrators

Administrative control across the forest.

---

## Service Accounts

Particularly those:

* Running critical services
* Managing infrastructure
* Holding delegated privileges

Examples:

* SQL Service Accounts
* Backup Service Accounts
* SCCM Service Accounts

---

## Backup Operators

Frequently overlooked but often capable of accessing sensitive data.

---

## PKI Administrators

Manage certificate infrastructure and trust relationships.

---

# BloodHound Analysis Workflow

## Step 1 – Identify High Value Targets

Review:

* Domain Controllers
* Domain Admins
* Enterprise Admins
* PKI Systems
* Identity Infrastructure

---

## Step 2 – Review Attack Paths

Analyze:

* Shortest Paths to High Value Targets
* Privilege Relationships
* Group Memberships
* Session Exposure

---

## Step 3 – Evaluate Exposure

Determine:

* Number of attack paths
* Required privileges
* Potential business impact

---

## Step 4 – Prioritize Findings

Focus on:

* Easily exploitable paths
* Excessive permissions
* Tier 0 exposure

---

# Common BloodHound Indicators

When analyzing BloodHound data, pay particular attention to:

## Shortest Paths to Domain Admin

Direct or indirect privilege escalation opportunities.

---

## Sessions

Privileged users logged onto lower-trust systems.

---

## Local Administrator Relationships

Administrative access chains across systems.

---

## ACL-Based Privileges

Permissions such as:

* GenericAll
* GenericWrite
* WriteDACL
* WriteOwner
* AddMember
* ForceChangePassword

---

## Delegation Relationships

Potential abuse of:

* Unconstrained Delegation
* Constrained Delegation
* Resource-Based Constrained Delegation

---

# Enterprise Risks

Poorly protected High Value Targets may lead to:

* Domain compromise
* Forest compromise
* Credential theft
* Long-term persistence
* Data exposure

---

# Defensive Considerations

Organizations should:

* Clearly identify Tier 0 assets
* Implement administrative tiering
* Restrict privileged logons
* Review delegated permissions
* Monitor privileged account activity
* Continuously analyze attack paths

---

# Assessment Checklist

During an Active Directory assessment:

* Identify all High Value Targets
* Map privilege relationships
* Review administrative groups
* Analyze attack paths
* Validate exposure
* Assess business impact
* Provide remediation recommendations

---

# References

* SpecterOps Research
* BloodHound Documentation
* Microsoft Enterprise Access Model
* MITRE ATT&CK
* Microsoft Security Guidance
