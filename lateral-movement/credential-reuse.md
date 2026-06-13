# Credential Reuse

## Overview

Credential reuse remains one of the most common enablers of lateral movement within enterprise environments.

Attackers frequently leverage reused administrative credentials to expand access rapidly across systems.

---

# Common Scenarios

## Shared Local Administrator Passwords

The same password used across multiple hosts.

---

## Reused Service Account Credentials

Service accounts sharing passwords across systems.

---

## Administrative Account Reuse

Privileged accounts used broadly throughout the environment.

---

# Enterprise Risks

* Rapid lateral movement
* Administrative compromise
* Domain escalation

---

# Assessment Workflow

1. Identify administrative relationships
2. Review password management practices
3. Analyze credential exposure
4. Evaluate attack path expansion

---

# Defensive Recommendations

* Implement LAPS
* Use unique passwords
* Restrict privileged account usage
* Enforce administrative tiering
