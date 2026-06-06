# Kerberoasting Attack Workflow

## Overview

Kerberoasting follows a predictable attack chain that transforms a low-privileged domain account into a potential privilege escalation opportunity.

The attack is particularly attractive because password cracking occurs offline and generates limited visibility for defenders.

---

# Typical Workflow

## Phase 1 – Initial Access

Obtain:

* Valid domain credentials
* User-level access

---

## Phase 2 – Service Discovery

Identify:

* Service accounts
* SPNs
* Privileged services

---

## Phase 3 – Ticket Request

Request Kerberos service tickets associated with target service accounts.

---

## Phase 4 – Offline Analysis

Extract ticket material and perform password analysis outside the target environment.

---

## Phase 5 – Credential Recovery

Recover service account credentials when weak passwords are used.

---

## Phase 6 – Privilege Assessment

Determine:

* Group memberships
* Administrative rights
* Tier 0 exposure

---

## Phase 7 – Attack Path Expansion

Use recovered privileges to:

* Move laterally
* Escalate privileges
* Access critical systems

---

# Common Outcomes

* Administrative access
* Service account compromise
* Tier 0 exposure
* Domain escalation

---

# Business Impact

Successful Kerberoasting may provide access to:

* Critical servers
* Databases
* Backup infrastructure
* Identity systems

---

# References

* SpecterOps Research
* MITRE ATT&CK
