# ADCS Relay

## Overview

Active Directory Certificate Services significantly increase the impact of NTLM Relay attacks.

Attackers may abuse relayed authentication to obtain certificates enabling privilege escalation or persistence.

---

# Why ADCS Matters

Certificates may provide:

* Authentication capabilities
* Persistence
* Privilege escalation paths

---

# Common Risks

* Weak certificate templates
* Excessive enrollment permissions
* Misconfigured web enrollment services

---

# Enterprise Impact

Successful abuse may lead to:

* Domain compromise
* Long-term persistence
* Authentication abuse

---

# Defensive Considerations

* Harden certificate templates
* Restrict enrollment permissions
* Disable unnecessary NTLM authentication
