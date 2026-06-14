# Session Abuse

## Overview

Privileged sessions frequently create realistic attack paths within Active Directory environments.

Attackers often target systems where privileged users are actively logged in.

---

# Common Risks

## Administrative Sessions on Workstations

Domain administrators logged into lower-trust systems.

---

## Shared Jump Servers

Multiple privileged users sharing the same systems.

---

## Unrestricted Administrative Logons

Privileged users authenticating broadly across the environment.

---

# Potential Impact

* Credential theft
* Token abuse
* Privilege escalation
* Tier 0 compromise

---

# Assessment Methodology

1. Identify active sessions
2. Review privileged account exposure
3. Analyze attack paths
4. Validate privilege escalation opportunities

---

# Defensive Considerations

* Session isolation
* Privileged Access Workstations
* Restricted administrative logons
* Tiered administration
