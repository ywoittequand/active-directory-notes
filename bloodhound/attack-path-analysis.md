# Attack Path Analysis

## Overview

BloodHound is not simply a visualization tool. Its primary purpose is to identify and analyze attack paths that may allow an attacker to move from a low-privileged position to high-value targets within an Active Directory environment.

Attack path analysis helps security professionals understand how privilege relationships, delegation, sessions, and administrative access combine to create escalation opportunities.

The objective is not to identify individual vulnerabilities but to understand the complete attack chain.

---

# What is an Attack Path?

An attack path is a sequence of relationships that allows an attacker to move from an initial foothold to a privileged asset.

Typical attack paths may involve:

* Group memberships
* ACL abuse
* Session exposure
* Delegation misconfigurations
* Local administrator rights
* Service account privileges

---

# Attack Path Analysis Methodology

## Step 1 – Define Starting Point

Determine the attacker's initial position.

Examples:

* Standard domain user
* Compromised workstation
* Service account
* Application server

Key Question:

What privileges are already available?

---

## Step 2 – Identify High Value Targets

Prioritize:

* Domain Controllers
* Domain Admins
* Enterprise Admins
* Certificate Authorities
* Identity Management Systems

Key Question:

What assets would significantly impact the organization if compromised?

---

## Step 3 – Review Shortest Paths

BloodHound automatically identifies shortest paths to target assets.

Focus on:

* Direct paths
* Multi-step paths
* Hidden privilege chains

Key Question:

How many actions are required to reach the target?

---

## Step 4 – Analyze Privilege Relationships

Review dangerous permissions such as:

* GenericAll
* GenericWrite
* WriteDACL
* WriteOwner
* AddMember
* ForceChangePassword

Key Question:

Can the attacker modify, control, or escalate privileges through these relationships?

---

## Step 5 – Review Session Exposure

Analyze active sessions involving:

* Administrators
* Privileged service accounts
* Tier 0 personnel

Key Question:

Can privileged credentials be exposed through session access?

---

## Step 6 – Validate Attack Feasibility

Determine:

* Required privileges
* Required access
* Operational constraints
* Potential detection opportunities

Key Question:

Is the attack path realistic?

---

# Common Attack Path Categories

## Administrative Access Paths

Examples:

* Local Administrator Rights
* Administrative Groups
* Privileged Remote Access

Risk:

Rapid lateral movement.

---

## ACL-Based Attack Paths

Examples:

* GenericAll
* WriteDACL
* AddMember

Risk:

Privilege escalation without credential theft.

---

## Session-Based Attack Paths

Examples:

* Exposed Domain Admin sessions
* Privileged user logons

Risk:

Credential theft and token abuse.

---

## Delegation-Based Attack Paths

Examples:

* Unconstrained Delegation
* Resource-Based Constrained Delegation

Risk:

Authentication abuse and privilege escalation.

---

## Service Account Paths

Examples:

* Kerberoastable accounts
* Excessive service account privileges

Risk:

Indirect administrative access.

---

# Prioritization Framework

When multiple attack paths exist, prioritize based on:

### Impact

What level of access is obtained?

### Complexity

How difficult is exploitation?

### Detection Risk

How likely is detection?

### Business Impact

What assets become accessible?

---

# Reporting Considerations

For each identified attack path:

* Starting Point
* Target Asset
* Required Steps
* Required Privileges
* Potential Impact
* Recommended Remediation

The goal is to provide actionable risk information rather than simply listing technical findings.

---

# References

* BloodHound Documentation
* SpecterOps Research
* Microsoft Security Guidance
* MITRE ATT&CK
