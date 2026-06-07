# ACL Abuse

## Overview

Access Control Lists (ACLs) define permissions applied to Active Directory objects.

Misconfigured ACLs frequently create hidden privilege escalation opportunities.

---

## Dangerous Permissions

### GenericAll

Full control over an object.

Potential Impact:

* Account takeover
* Password reset
* Group modification

---

### GenericWrite

Modification of object attributes.

Potential Impact:

* SPN abuse
* Shadow credentials
* Escalation opportunities

---

### WriteDACL

Permission modification.

Potential Impact:

* Privilege escalation
* Persistence

---

### WriteOwner

Ownership modification.

Potential Impact:

* ACL takeover
* Escalation

---

### AddMember

Group membership modification.

Potential Impact:

* Administrative access

---

### ForceChangePassword

Password reset without current password.

Potential Impact:

* Account compromise

---

## Assessment Workflow

1. Enumerate ACLs
2. Identify dangerous permissions
3. Map attack paths
4. Validate business impact

---

## Defensive Considerations

* ACL reviews
* Delegation governance
* Privileged group monitoring
