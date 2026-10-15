# CR-01 — Privacy-aware engagement trend verification

**Type:** Documentation and test-design change for Experiment 9  
**Branch:** `feature/privacy-aware-trends`  
**Status:** Merged into the `Version1` baseline for the SCM practical

## Change summary

Add a version-controlled verification record for the EEWMS requirement to provide aggregate engagement trends while protecting small employee groups. This change organizes the acceptance checks; it does not claim that EEWMS product code was implemented or deployed.

## Basis and acceptance checks

- Trend output is aggregate and does not expose individual survey responses.
- Group-level output is permitted only when the organization's configured privacy minimum is met.
- Results below that configured threshold are suppressed or combined, according to the approved policy.
- The threshold value remains an organization-defined configuration; this record introduces no numeric cutoff.
- Automated engagement or sentiment indicators remain decision-support signals, not definitive judgments about an employee.

## Verification examples

1. Configure a group that meets the approved reporting threshold; verify only aggregate trend data is returned.
2. Configure a group below the threshold; verify the restricted result is suppressed or combined.
3. Inspect the output to confirm no individual response or identity is exposed.

## Scope note

This is a documentation/test-design artifact for the SCM exercise. Production behavior, legal/privacy approval, and the organization's numeric threshold remain outside the scope of this change record.
