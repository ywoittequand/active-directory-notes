# BloodHound Collection Methods

## Overview

BloodHound relies on data collection from Active Directory environments to identify privilege relationships, attack paths, and potential escalation opportunities.

The quality and scope of the collected data directly impact the effectiveness of attack path analysis.

Understanding collection methods is essential during internal penetration tests, assumed breach scenarios, and Active Directory security assessments.

---

## Collection Objectives

The primary goals of data collection are:

* Identify users and groups
* Enumerate computers and servers
* Discover privilege relationships
* Collect session information
* Analyze ACLs and delegated permissions
* Identify attack paths toward high-value targets

---

## SharpHound

### Overview

SharpHound is the official BloodHound data collector.

It gathers information from Active Directory and exports the results for analysis within BloodHound.

---

## Common Collection Categories

### Group Memberships

Collects relationships between:

* Users
* Groups
* Administrative groups

Purpose:

* Identify privilege inheritance
* Discover nested groups
* Analyze administrative access

---

### Local Administrator Rights

Collects:

* Local administrator memberships
* Administrative relationships between hosts

Purpose:

* Identify lateral movement opportunities
* Discover administrative chaining

---

### Session Collection

Collects:

* Active user sessions
* Logged-on users

Purpose:

* Identify credential exposure
* Discover privileged sessions

---

### ACL Collection

Collects:

* Object permissions
* Delegated rights
* Ownership relationships

Purpose:

* Identify privilege escalation opportunities
* Discover hidden attack paths

---

### Trust Relationships

Collects:

* Domain trusts
* Forest trusts

Purpose:

* Assess cross-domain attack paths
* Identify trust-based escalation opportunities

---

## Collection Strategies

### Standard Collection

Suitable for:

* Internal penetration tests
* Initial Active Directory assessments

Focus:

* Core privilege relationships
* Group memberships
* Administrative paths

---

### Comprehensive Collection

Suitable for:

* Red Team engagements
* Assumed breach scenarios

Focus:

* Sessions
* ACLs
* Delegation
* High-value targets

---

### Targeted Collection

Suitable for:

* Large environments
* Specific investigations

Focus:

* Critical systems
* Privileged accounts
* Tier 0 assets

---

## Assessment Methodology

### Step 1 – Define Scope

Identify:

* Domains
* Forests
* Critical systems
* Assessment objectives

---

### Step 2 – Collect Data

Gather:

* Group memberships
* Sessions
* ACLs
* Local administrator relationships

---

### Step 3 – Validate Data Quality

Review:

* Missing objects
* Incomplete session data
* Collection errors

---

### Step 4 – Import into BloodHound

Analyze:

* High-value targets
* Attack paths
* Privilege relationships
* Tier 0 exposure

---

## Common Findings

Typical discoveries include:

* Excessive privileges
* Local administrator reuse
* Service account exposure
* Session exposure
* Delegation abuse
* ACL misconfigurations

---

## Enterprise Risks

Poorly managed privilege relationships may lead to:

* Privilege escalation
* Lateral movement
* Domain compromise
* Tier 0 exposure

---

## Defensive Considerations

Organizations should:

* Review delegated permissions
* Limit excessive privileges
* Monitor privileged sessions
* Harden administrative boundaries
* Perform regular attack path analysis

---

## References

* BloodHound Documentation
* SpecterOps Research
* Microsoft Security Guidance
* MITRE ATT&CK
