---
name: Change Review
about: Pre-deployment review for changes with meaningful production risk
title: "[CHANGE REVIEW] <change description>"
labels: change-review
---

## Change Summary

| Field | Value |
|---|---|
| Change description | |
| Services affected | |
| Author | |
| Reviewer(s) | |
| Planned deployment window | |
| Change type | Code / Config / Infra / Data migration / Third-party |

## Risk Level

- [ ] Low — routine, well-tested, easily reversible
- [ ] Medium — touches shared infra or has moderate blast radius
- [ ] High — touches critical path, data, or has limited rollback options

## What Changes

Plain description of what's different after this change. Link the PR(s).

## Why Now

Business or technical reason for this change, and why this timing.

## Risk & Rollback

- What could go wrong?
- How would we detect it if it did?
- Rollback plan — is it a simple revert, or does it need a separate [Service Rollback](./02-service-rollback.md) process (e.g., due to migrations)?
- Estimated time to rollback if needed

## Testing Completed

- [ ] Unit / integration tests passing
- [ ] Tested in staging with production-like data/traffic
- [ ] Peer reviewed
- [ ] Load tested (if relevant)

## Deployment Plan

- [ ] Deploying during low-traffic window / has approval to deploy during peak
- [ ] Canary or phased rollout planned
- [ ] On-call aware and available during deployment window
- [ ] Monitoring dashboards open during and after deployment

## Approval

| Reviewer | Role | Approved | Date |
|---|---|---|---|
| | | ☐ | |

---
*Reserve this for changes with real risk — not every PR needs a formal change review. Use judgement calibrated by blast radius, not by team habit.*
