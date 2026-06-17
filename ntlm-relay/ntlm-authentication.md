# NTLM Authentication

## Overview

NTLM is a legacy authentication protocol still widely used in Active Directory environments.

Although Kerberos is preferred, NTLM remains present for compatibility reasons.

---

# NTLM Characteristics

* Challenge-response protocol
* Legacy authentication support
* Common in mixed environments

---

# Security Limitations

* Susceptible to relay attacks
* Weak mutual authentication
* Legacy dependency

---

# Enterprise Exposure

NTLM remains enabled due to:

* Legacy systems
* Third-party applications
* Operational dependencies

---

# Defensive Considerations

* Reduce NTLM usage
* Enforce SMB signing
* Monitor NTLM activity
