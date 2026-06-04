# Common Findings

## Overview

BloodHound assessments frequently reveal recurring privilege and configuration issues within Active Directory environments.

While individual organizations differ, many attack paths originate from the same categories of exposure.

Understanding these common findings helps prioritize remediation efforts and reduce attack surface.

---

# Excessive Privileges

## Description

Users or groups possess privileges beyond operational requirements.

Examples:

* Unnecessary administrative rights
* Broad delegated permissions
* Excessive group memberships

Potential Impact:

* Privilege escalation
* Expanded attack paths
* Increased blast radius

---

# Local Administrator Reuse

## Description

Identical local administrator credentials exist across multiple systems.

Potential Impact:

* Lateral movement
* Credential reuse
* Rapid environment compromise

Common Indicator:

Large numbers of systems sharing administrative relationships.

---

# Privileged Session Exposure

## Description

Privileged accounts authenticate to lower-trust systems.

Potential Impact:

* Credential theft
* Token abuse
* Domain escalation

Common Indicator:

Domain Admin sessions on user workstations.

---

# ACL Misconfigurations

## Description

Delegated permissions allow modification of users, groups, or critical objects.

Examples:

* GenericAll
* GenericWrite
* WriteDACL
* AddMember

Potential Impact:

* Privilege escalation
* Hidden attack paths
* Persistence

---

# Service Account Exposure

## Description

Service accounts possess excessive privileges or weak credential management.

Potential Impact:

* Kerberoasting
* Administrative access
* Lateral movement

Common Indicator:

Privileged service accounts with broad system access.

---

# Delegation Misconfigurations

## Description

Improper delegation settings expose authentication workflows.

Examples:

* Unconstrained Delegation
* Misconfigured RBCD

Potential Impact:

* Authentication abuse
* Privilege escalation
* Domain compromise

---

# Tier 0 Exposure

## Description

High-value assets remain reachable through indirect attack paths.

Examples:

* Domain Controllers
* Enterprise Admins
* PKI Infrastructure

Potential Impact:

* Complete domain compromise

Common Indicator:

Multiple shortest paths originating from standard users.

---

# Group Nesting Complexity

## Description

Deeply nested groups create hidden privilege inheritance.

Potential Impact:

* Difficult privilege management
* Unintended administrative access

Common Indicator:

Complex membership chains visible within BloodHound.

---

# Weak Administrative Boundaries

## Description

Administrative access extends beyond intended security tiers.

Potential Impact:

* Tier crossing
* Attack path expansion
* Reduced containment

Common Indicator:

Administrative relationships spanning multiple trust zones.

---

# Common Remediation Themes

Organizations should prioritize:

* Least privilege enforcement
* Administrative tiering
* Session isolation
* Privileged access management
* ACL reviews
* Service account hardening
* Continuous attack path analysis

---

# Risk-Based Prioritization

Not all findings carry the same level of risk.

Priority should be given to findings that:

* Lead directly to Tier 0 assets
* Require few attack steps
* Involve privileged credentials
* Enable persistence

---

# Assessment Takeaways

BloodHound findings should be viewed as attack path indicators rather than isolated vulnerabilities.

The objective is to understand how multiple weaknesses combine to create realistic compromise scenarios.

Effective remediation focuses on breaking attack chains rather than addressing individual nodes in isolation.

---

# References

* BloodHound Documentation
* SpecterOps Research
* Microsoft Enterprise Access Model
* MITRE ATT&CK
