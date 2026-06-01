# BloodHound Analysis Methodology

## Objectives

BloodHound helps identify hidden privilege relationships and attack paths inside Active Directory environments.

## Key Analysis Areas

- High-value targets
- Tier 0 exposure
- Local admin relationships
- Session exposure
- Delegated permissions
- Kerberoastable accounts

## Common Analysis Workflow

1. Identify Domain Admin exposure
2. Review shortest paths
3. Analyze local admin chaining
4. Review session data
5. Validate escalation opportunities

## Common Risks

- Excessive privilege inheritance
- Hidden delegated permissions
- Unrestricted lateral movement
- Weak administrative boundaries
