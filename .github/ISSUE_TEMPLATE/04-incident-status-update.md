---
name: Incident Status Update
about: Standardized format for communicating incident status to stakeholders
title: "[STATUS UPDATE] <incident-id> — Update #<n>"
labels: incident, communication
---

## Quick Status

| Field | Value |
|---|---|
| Incident ID | |
| Current status | Investigating / Identified / Monitoring / Resolved |
| Severity | |
| Time of this update (UTC) | |
| Next update expected by (UTC) | |

## What's Happening

One or two plain-language sentences. No jargon — this may be read by non-technical stakeholders or customers.

*Example: "We're seeing elevated error rates on checkout for a subset of users. We've identified the likely cause and are testing a fix."*

## Impact

- Who is affected (all users / some users / internal only)?
- What functionality is degraded or unavailable?

## What We're Doing

- Current mitigation or investigation steps in plain language.

## What's Next

- Expected next milestone (e.g., "deploying a fix," "confirming root cause").
- Time of next scheduled update.

---

### Internal-only notes (do not include in customer-facing version)

- Technical detail for internal stakeholders
- Links to dashboards, logs, related PRs

---
*Send updates on a predictable cadence (e.g., every 30 min for SEV-1) even if the update is "no change yet" — silence is worse than a repeated update.*
